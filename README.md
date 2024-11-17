# Python
Python2

import math


points = [(1, 2), (3, 4), (5, 6), (7, 8)]


def euclideanDistance(point1, point2):
    x1, y1 = point1
    x2, y2 = point2
    return math.sqrt((x2 - x1)**2 + (y2 - y1)**2)


distances = []
for i in range(len(points)):
    for j in range(i + 1, len(points)):  # Her çifti bir kez hesapla
        distances.append(euclideanDistance(points[i], points[j]))


min_distance = min(distances)
print(f"Minimum Öklid mesafesi: {min_distance}")
