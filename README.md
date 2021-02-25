# lg2-
package  Exceções_ControleErros ;

public  class  ExeptionGenerica {
	
	public  static  void  main ( String [] args ) {
	
	int [] numeros = { 4 , 8 , 16 , 32 , 64 , 128 };
	int [] denom = { 2 , 0 , 4 , 8 , 0 };
	
	para ( int i =  0 ; i < numeros . comprimento; i ++ ) {
		
		tente {
			
			Sistema . para fora . println (numeros [i] +  " / "  + denom [i] +  " = "  + (numeros [i] / denom [i]));
		 }
		
		catch ( exceção e) {
			
			Sistema . para fora . println (e . getMessage ());		
			e . printStackTrace ();
		}
		
	 }
	
  }

}

pegadinha
package  Exceções_ControleErros ;

public  class  FinalmentePegadinha {
	
	public  static  void  main ( String [] args ) {

	int [] numeros = { 4 , 8 , 16 , 32 , 64 , 128 };
	int [] denom = { 2 , 0 , 4 , 8 , 0 };
	
	para ( int i =  0 ; i < numeros . comprimento; i ++ ) {
		
		tente {
			Sistema . para fora . println (numeros [i] +  " / "  + denom [i] +  " = "  + (numeros [i] / denom [i]));
		 }
		
		catch ( ArithmeticException e) {
			
			Sistema . para fora . println ( " Erro ao dividir pro zero " );	
			Sistema . saída ( 0 );
		}
		
        catch ( ArrayIndexOutOfBoundsException e) {
			
			Sistema . para fora . println ( " Posição do array inválida " );
			Sistema . saída ( 0 );
		}
		
		finalmente {
			
			Sistema . para fora . println ( " Essa linha é impressa sempre após o try ou o catch " );
		}
		
	 }
	
   }

}

multiplos  cathc
package  Exceções_ControleErros ;

public  class  MultiplosCatch {

	public  static  void  main ( String [] args ) {
		
		int [] numeros = { 4 , 8 , 16 , 32 , 64 , 128 };
		int [] denom = { 2 , 0 , 4 , 8 , 0 };
		
		para ( int i =  0 ; i < numeros . comprimento; i ++ ) {
			
			tente {
				Sistema . para fora . println (numeros [i] +  " / "  + denom [i] +  " = "  + (numeros [i] / denom [i]));
			 }
			
			catch ( ArithmeticException e) {
				
				Sistema . para fora . println ( " Erro ao dividir pro zero " );		
			}
			
            catch ( ArrayIndexOutOfBoundsException e) {
				
				Sistema . para fora . println ( " Posição do array inválida " );		
			}
			
		 }
		
	}

}

package  Exceções_ControleErros ;

public  class  MultiplosCatchGenerico {
	
    public  static  void  main ( String [] args ) {
 		
		int [] numeros = { 4 , 8 , 16 , 32 , 64 , 128 };
		int [] denom = { 2 , 0 , 4 , 8 , 0 };
		
		para ( int i =  0 ; i < numeros . comprimento; i ++ ) {
			
			tente {
				Sistema . para fora . println (numeros [i] +  " / "  + denom [i] +  " = "  + (numeros [i] / denom [i]));
			 }
			
			catch ( ArithmeticException e) {
				
				Sistema . para fora . println ( " Erro ao dividir pro zero " );		
			}
			
            pegar ( lançável e) {
				
				Sistema . para fora . println ( " Ocorreu um erro " );		
			}
			
		 }
		
	}

}

package  Exceções_ControleErros ;

public  class  MultiplosCatchJava7 {
	
    public  static  void  main ( String [] args ) {
		
		int [] numeros = { 4 , 8 , 16 , 32 , 64 , 128 };
		int [] denom = { 2 , 0 , 4 , 8 , 0 };
		
		para ( int i =  0 ; i < numeros . comprimento; i ++ ) {
			
			tente {
				Sistema . para fora . println (numeros [i] +  " / "  + denom [i] +  " = "  + (numeros [i] / denom [i]));
			 }
			
			catch ( ArithmeticException  |  ArrayIndexOutOfBoundsException e) {
				
				Sistema . para fora . println ( " Aconteceu um erro " );		
			}
			
		 }
		
    }

}

package  Exceções_ControleErros ;

import  java.util.Scanner ;

public  class  UsandoThrows {

	public  static  void  main ( String [] args ) {
		
		Sistema . para fora . println ( " Entre com um número decimal " );
		tente {
			duplo núm = leNumero ();
			Sistema . para fora . println ( " Você digitou "  + num);
		} catch ( exceção e) {
			Sistema . para fora . println ( " Entrada inválida " );
			e . printStackTrace ();
		}

	}

	public  static  double  leNumero () lança  Exception {
		Varredura do scanner =  novo  scanner ( sistema . In);
		double num = scan . nextDouble ();
		return num;
	}
}
