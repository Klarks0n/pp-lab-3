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
import geometry.ColoredCircle;
import geometry.Point;
public class Main {
    public static void main(String[] args) {
        Point center = new Point(0, 0);
        double radius = 5,0;
        String color = "orange";
        ColoredCircle coloredCircle = new ColoredCircle(center, radius, color);
        System.out.println("Center: (" + coloredCircle.getCenter().getX() + ", " + coloredCircle.getCenter().getY() + ")");
        System.out.println("Radius: " + coloredCircle.getRadius());
        System.out.println("Color: " + coloredCircle.getColor());
        System.out.println("Perimeter: " + coloredCircle.calculatePerimeter());
        System.out.println("Area: " + coloredCircle.getArea());
    }
}
