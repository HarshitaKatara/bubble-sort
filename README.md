# bubble-sort
// sorting by using bubble sort for a large number of elements or any integer type array.//
package com.company;
import java.util.Arrays;
import java.util.Scanner;
public class Main {

   public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter size: ");
        int n = sc.nextInt();
        int temp;
        int a[] = new int[n];
        System.out.print("Enter all the elements: ");
        for (int i = 0; i < n; i++) {
            a[i] = sc.nextInt();
        }
        for(int i=0; i<n; i++){
          int flag = 0;
            for(int j=0; j<n-1-i; j++){
                if(a[j] > a[j+1]){
                   temp = a[j];
                   a[j] = a[j+1];
                   a[j+1] = temp;
                   flag = 1;
                }
            }
            if(flag == 0){
               break;
            }
        }
        for(int i=0; i<n; i++) {
            System.out.println(a[i]+" ");
        } 
    }
}
