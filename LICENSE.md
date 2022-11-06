# Rachel Gupta finds Max Digit  #

import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */
        Scanner sc = new Scanner(System.in);
        String str1 = sc.nextLine();
        int n = str1.length();
        int[] frqarr = new int[10];
        
        for(int i=0; i<n; i++){
            char ch = str1.charAt(i);
            int index = ch - 48;
            frqarr[index]++;
        }
        int mxFrq = 0;
        char ch = '-';
        for(int i=0; i<10; i++){
            if(frqarr[i] > mxFrq){
                mxFrq = frqarr[i];
                ch = (char)(i+48);
            }
        }
        System.out.print(ch);
    }
}
