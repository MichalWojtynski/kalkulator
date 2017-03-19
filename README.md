# kalkulator

package bla;

import java.io.FileNotFoundException;
import java.io.IOException;
import java.util.Scanner;

import javax.script.ScriptException;

public class Kalkulator {

	/*
	 * Wypisanie Menu i prosba o wybor czy chcemy 
	 * wprowadzic dane z pliku czy pobrac od uzytkownika
	 */
	
	public static void main(String[] args) throws ScriptException, FileNotFoundException, IOException{ 
	{
		
		System.out.println("-------------MENU--------------");
		System.out.println("-1-Wprowadz dane wlasnorecznie."); 
		System.out.println("-2-Wprowadz dane z pliku."); 
		System.out.println("-0-Koniec programu."); 
	
		
	      @SuppressWarnings("resource")
	      
		Scanner odczyt = new Scanner(System.in); 
	 
	       String wybor = odczyt.nextLine();
	       System.out.println("Twoj wybor: " + wybor); 
	       int wyb = Integer.valueOf(wybor);
	       if(wyb == 1)
	       {
	    	   Uzytkownik uzytkownik = new Uzytkownik();
	    	   uzytkownik.wprowadzdane();
	       }
	       else if( wyb == 2)
	       {
	    	   Plik plik = new Plik();
	    	   plik.skannapis();
	       }
	       else if(wyb == 0 )
	       {
	    	   System.out.println("----------KONIEC-------- " ); 
	    	   System.exit(0);
	       }
	       else
	       {
	    	   main(null);
	       }
	      
	      
	}

}
}

