# Java-Password-Generator
// This is a java Password Generator

import java.util.Random;
public class PasswordGenerator {
	 public static void main(String[]args){
    	 int length = 8;// password length
    	 System.out.println(generatePswd(length));
    	 }
     static char[] generatePswd(int len){
    	 System.out.println("your password:");
    	 String charsCaps = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
    	 String chars = "abcdefghijklmnopqrstuvwxyz";
    	 String nums = "0123456789";
    	 String symbols = "!@#$%^&*_<>?=+-";// feel free to add any other symbols, i did not add all symbols
    	 String passSymbols = charsCaps + chars + nums+symbols;
    	 Random rnd = new Random();
    	 char[]password  = new char[len];
    	 int index = 0;
    	 for(int i = 0;i<len;i++){
    		 password[i]= passSymbols.charAt(rnd.nextInt(passSymbols.length()));
    	 }
    	 return password;
       }
	}
