# RavProject

git init 
git remote add origin https://github.com/Ravenna2/RavProject/blob/RavProject-edits/README.md
git push -u origin RavProject-edits

import java.util.Random;


    public abstract class Arma extends Item {
        private int danoMAX;
        private int durabilidade;
        public Arma(String nome,int danoMAX, int durabilidade){
           this.nome = nome;
           this.danoMAX = danoMAX;
           this.durabilidade = durabilidade;
    }
       
        @Override
    
     public String examinar(){
         String dado = this.nome + String.valueOf(this.danoMAX) + String.valueOf(this.durabilidade);
            
         return dado;}

     public int atacar(){
         if(durabilidade == 0){
             return 0;}
         else {
             this.durabilidade = this.durabilidade - 1;
    
             Random rd = new Random();
  
             int dano = rd.nextInt(this.danoMAX);
    
              return dano;
    }}
    
public abstract boolean usaApenasUmaMao();
        }
        
        
        
         public class AtaqueaDistancia extends Arma{

             public AtaqueaDistancia(String nome, int danoMAX, int durabilidade) {
         
        	   super(nome, danoMAX, durabilidade);
    }

   
        @Override
    
    public boolean usaApenasUmaMao() {
        return false;
    }
    
}

