package geometry;
public class Point {
    private double x;
    private double y;
    public Point(double x, double y) {
        this.x = x;
        this.y = y;
    }
    public double getX() {
        return x;
    }
    public double getY() {
        return y;
    }
}
package geometry;
public class Circle {
    private Point center;
    private double radius;
    public Circle(Point center, double radius) {
        this.center = center;
        this.radius = radius;
    }
    public Point getCenter() {
        return center;
    }
    public double getRadius() {
        return radius;
    }
    public double calculatePerimeter() {
        return 2 * Math.PI * radius;
    }
    public double getArea() {
        return Math.PI * radius * radius;
    }
}
import geometry.Circle;
public class Main {
    public static void main(String[] args) {
        Point center = new Point(0, 0);
        double radius = 5.0;
        Circle circle = new Circle(center, radius);
        System.out.println("Center: (" + circle.getCenter().getX() + ", " + circle.getCenter().getY() + ")");
        System.out.println("Radius: " + circle.getRadius());
        System.out.println("Perimeter: " + circle.calculatePerimeter());
        System.out.println("Area: " + circle.getArea());
    }
}
