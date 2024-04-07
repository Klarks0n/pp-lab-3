package geometry;
public class Rectangle {
    private double length;
    private double width;
    public Rectangle(double length, double width) {
        this.length = length;
        this.width = width;
    }
    public double getArea() {
        return length*width;
    }
    public double calculatePerimeter() {
        return 2*(length + width);
    }
}
import geometry.Rectangle;
public class Main {
    public static void main(String[] args) {
        Rectangle rectangle = new Rectangle(3, 7);
        System.out.println("Rectangle Area: " + rectangle.getArea());
        System.out.println("Rectangle Perimeter: " + rectangle.calculatePerimeter());
    }
}
