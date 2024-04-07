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
    public double getArea() {
        return Math.PI * radius;
    }
}
package geometry;
public class ColoredCircle extends Circle {
    private String color;
    public ColoredCircle(Point center, double radius, String color) {
        super(center, radius);
        this.color = color;
    }
    public String getColor() {
        return color;
    }
}
import geometry.Circle;
import geometry.ColoredCircle;
import geometry.Point;
public class Main {
    public static void main(String[] args) {
        Circle[] circles = {
            new Circle(new Point(0, 0), 5),
            new Circle(new Point(2, 3), 7),
            new ColoredCircle(new Point(1, 1), 3, "blue"),
            new ColoredCircle(new Point(-2, -2), 4, "green")
        };
        for (Circle circle : circles) {
            double area = circle.getArea();
            System.out.println("Area: " + area);
            if (circle instanceof ColoredCircle) {
                String color = ((ColoredCircle) circle).getColor();
                System.out.println("Color: " + color);
            }
        }
    }
}
