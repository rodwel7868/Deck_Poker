# Deck_Poker
Cartas de Poker

package Logica;

import LogicaCartas.cartas;
import java.util.List;
import java.util.Collections;
import java.util.ArrayList;

public class Decks {
    
    private static List<cartas> Carta;

    public static void main(String[] args) {
        
        Carta = new ArrayList<>();
        
        String[] palo = {"Diamante", "Corazon", "Trevol", "Pica"};
        String[] valor = {"A", "2", "3", "4", "5", "6", "7", "8", "9", "10", "J", "Q", "K"};
        
        for (String pal : palo){
            
            for (int i = 0; i < valor.length; i ++){
                
                String val = valor [i]; 
                String col = "";
                
                if ((pal == "Trebol") || (pal == "Pica")){
                    col = "Negro";
                }else{
                    col = "Rojo";
                }
                cartas cart = new cartas(pal, col, val);
                Carta.add(cart);
            }
        }
        
        shuffle();
        head();
        pick();
        hand();
    }
    
    public static void shuffle(){
        Collections.shuffle(Carta);
        System.out.println("Se mezcla el mazo");
    }
    
    public static void head(){
        if (Carta.size() > 0){
            cartas cart = Carta.remove(0);
            System.out.println(cart.toString());
            System.out.println("Quedan " + Carta.size()+ " cartas en el mazo.");
        }
        
    }
    
    public static void pick() {
        if (Carta.size() > 0) {
            int randomIndex = (int) (Math.random() * Carta.size());
            cartas card = Carta.remove(randomIndex);
            System.out.println(card.toString());
            System.out.println("Quedan " + Carta.size() + " cartas en el mazo.");
        }
    }
        
    public static void hand() {
        if (Carta.size() >= 5) {
            for (int i = 0; i < 5; i++) {
                cartas card = Carta.remove(0);
                System.out.println(card.toString());
            }
            System.out.println("Quedan " + Carta.size() + " cartas en el maso.");
        }
    }
    
    public int getRemainingCards() {
        return Carta.size();
    }
}


package LogicaCartas;

public class cartas {
    
    private String palo;
    private String color;
    private String valor;
    
    public cartas(String palo,String color, String valor){
        this.palo = palo;
        this.color = color;
        this.valor = valor;
    }

    public String getPalo() {
        return palo;
    }

    public void setPalo(String palo) {
        this.palo = palo;
    }

    public String getColor() {
        return color;
    }

    public void setColor(String color) {
        this.color = color;
    }

    public String getValor() {
        return valor;
    }

    public void setValor(String valor) {
        this.valor = valor;
    }
    
    @Override
    public String toString(){
        return valor + " " + palo + " " + color + " ";
    
    }
}

