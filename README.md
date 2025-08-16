Arrays.sort(nums, Comparator.comparingLong(Pair::v));


import java.util.*;

class Point {
    int x, y;
    Point(int x, int y) {
        this.x = x;
        this.y = y;
    }
}

public class Main {
    public static void main(String[] args) {
        List<Point> points = new ArrayList<>();
        points.add(new Point(5, 2));
        points.sort((p1, p2) -> {
            if (p1.x != p2.x) {
                return Integer.compare(p2.x, p1.x); // x descending
            } else {
                return Integer.compare(p2.y, p1.y); // y descending if x equal
            }
        });
         for (Point p : points) {
            System.out.println(p.x + " " + p.y);
        
