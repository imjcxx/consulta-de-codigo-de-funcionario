# Consulta-de-C-digo-de-Funcionario
Sistema rápido para checar o desempenho de vendedores.
import java.util.Scanner;
/**
 *
 * @author joana
 */
public class ConsultaDeFuncionario {
    public static double totalVendido(String Cod){ 
        double valorReturn = 0;
      //preenchendo o vetor com código de vendedor.
        String [] vetorCod = {"G589","F461","H270","C116","Z348"};
       //preenchendo vetor com valor de vendas.
        double [] vetorVnd = {150,598,2.350,5.798,15.768};
        boolean encontrado = false;
       for(int i=0; i<vetorCod.length; i++){   
            
                if(Cod.equals(vetorCod[i])){
                    valorReturn = vetorVnd[i];
                  encontrado = true;
                         break;
                }
      } if(encontrado==false) {
                    System.out.println("Vendedor não encontrado");
                }
      
      return valorReturn;
    } 
     
    public static void main(String[]args){
        Scanner input = new Scanner (System.in);
         //{"G589","F461","H270","C116","Z348"}
       System.out.println("Digite seu código de identificação");
        String infCod = input.next();
        
       double valor = totalVendido(infCod);
        
        System.out.printf("O valor vendido pelo %s é %.2f", infCod,valor);
    }
}
