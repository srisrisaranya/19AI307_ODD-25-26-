# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:

Design a program where a Product model stores item info, and the view displays it. Implement a controller to update product price and refresh the view automatically.

## AIM:

To demonstrate the MVC (Model-View-Controller) design pattern in Java by managing and displaying product details

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the product name, price, code, and new price from the user.
4. Create a Product object with the given details (Model).
5. Create a ProductView object to display product information (View).
6. Create a ProductController object and connect the Model and View (Controller).
7. Display the initial product details using updateView().
8. Update the product price using updatePrice(newPrice).
9. Refresh and display the updated product details.
10. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: Saranya S
RegisterNumber:  212223110044
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class ProductManagementSystem {

    // ===== Model =====
    static class Product {
        private String name;
        private double price;
        private String code;

        // TODO: Constructor to initialize name, price, code
        public Product(String name, double price, String code) {
            this.name = name;
            this.price = price;
            this.code = code;
        }
        // TODO: Getter for name
         public String getName() {
            return name;
         }
        // TODO: Getter for price
        public double getPrice() {
            return price;
        }
        // TODO: Getter for code
         public String getCode() {
            return code;
        }
        // TODO: Setter for price
        public void setPrice(double price) {
            this.price = price;
        }
    }

    // ===== View =====
    static class ProductView {
        public void displayProduct(String name, double price, String code) {
            System.out.println("--- Product Details ---");
            System.out.println("Name : " + name);
            System.out.println("Price: " + price);
            System.out.println("Code : " + code);
        }
    }

    // ===== Controller =====
    static class ProductController {
        private Product product;
        private ProductView view;

        // TODO: Constructor to initialize product and view
        public ProductController(Product product, ProductView view) {
            this.product = product;
            this.view = view;
        }
        // TODO: Method updateView() → calls view.displayProduct()
         public void updateView() {
            view.displayProduct(product.getName(), product.getPrice(), product.getCode());
        }
        // TODO: Method updatePrice(double) → sets new price and refreshes view
          public void updatePrice(double newPrice) {
            product.setPrice(newPrice);
            updateView();
    }
    }

    // ===== Main Method =====
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // TODO: Take input - name, price, code, newPrice
        String name = sc.nextLine();
        double price = sc.nextDouble();
        sc.nextLine(); 
        String code = sc.nextLine();
        double newPrice = sc.nextDouble();
        // TODO: Create Product, View, and Controller objects
        Product product = new Product(name, price, code);
        ProductView view = new ProductView();
        ProductController controller = new ProductController(product, view);

        // TODO: Call controller.updateView()
         controller.updateView();
        // TODO: Call controller.updatePrice(newPrice)
        controller.updatePrice(newPrice);
        sc.close();
    }
}

```
## OUTPUT:

<img width="887" height="432" alt="image" src="https://github.com/user-attachments/assets/ac481375-8bef-4376-be4f-5be33dbc41e1" />


## RESULT:
The program successfully demonstrates the MVC design pattern by separating product data (Model), display logic (View), and control logic (Controller), and updates the product price while displaying the latest information.
