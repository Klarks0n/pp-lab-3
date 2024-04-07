package geometry;
public class Square extends Rectangle {
    public Square(double sideLength) {
        super(sideLength, sideLength);
    }
}
import geometry.Square;
public class Main {
    public static void main(String[] args) {
        Square square = new Square(3);
        System.out.println("Square Area: " + square.getArea());
        System.out.println("Square Perimeter: " + square.calculatePerimeter());
    }
}
