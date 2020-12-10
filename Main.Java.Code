package com.company;

import java.util.ArrayList;
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        ArrayList<purchases> catalog = new ArrayList<purchases>();
        ArrayList<inventory> stock = new ArrayList<inventory>();

        inventory I = new inventory();
        I.setItem("Bison Sweater");
        I.setPrice(55.99);
        stock.add(I);

        I = new inventory();
        I.setItem("Bison Tee");
        I.setPrice(14.99);
        stock.add(I);

        I = new inventory();
        I.setItem("Bison Hoodie");
        I.setPrice(23.99);
        stock.add(I);

        I = new inventory();
        I.setItem("Bison Bumpersticker");
        I.setPrice(4.99);
        stock.add(I);

        Scanner input = new Scanner(System.in);
        String item;
        double sum = 0.0;
        int index = -1;

        do {
            System.out.println("What item do you want to buy? If you are done write 'Finish Transaction':  ");
            item = input.nextLine();
            purchases order = new purchases();

            for (int i = 0; i < stock.size(); i++) {
                String test = stock.get(i).getItem();
                if (test.equals(item)) {
                    index = i;
                    String pi = stock.get(index).getItem();
                    double pp = stock.get(index).getPrice();
                    order.setPurchase_Item(pi);
                    order.setPurchase_Price(pp);
                    catalog.add(order);
                }
            }
        } while (!item.equalsIgnoreCase("Finish Transaction"));

        for (int i = 0; i < catalog.size(); i++) {
            System.out.println("You purchased: " + catalog.get(i).getPurchase_Item());
            double itemPrice=  catalog.get(i).getPurchase_Price();
            sum += itemPrice;
        }
        System.out.println("Your order sum is: " + sum);
        System.out.println("Your order has been placed! Thanks for shopping.");
        }
    }
