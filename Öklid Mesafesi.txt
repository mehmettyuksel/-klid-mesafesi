import math

# Points listesinin tanımlanması
points = [(2, 3), (5, 4), (1, 2), (7, 8), (9, 6)]

# Öklid mesafesi hesaplama fonksiyonu
def euclideanDistance(point1, point2):
    return math.sqrt((point2[0] - point1[0]) ** 2 + (point2[1] - point1[1]) ** 2)

# Mesafelerin hesaplanması ve saklanması
distances = []
for i in range(len(points)):
    for j in range(i + 1, len(points)):
        dist = euclideanDistance(points[i], points[j])
        distances.append(dist)

# Minimum mesafenin bulunması
min_distance = min(distances)
print("Minimum mesafe:", min_distance)
