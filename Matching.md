package strategistringmatch;

public class StrategiStringMatch {

    public static void main(String[] args) {
        
        String kalimat = "222131333232222322211113113113331113111123132212121213211212221332223";
        String[] kata = kalimat.split("(?<=\\G.{3})");
        System.out.println("SOAL 1");
        System.out.println("Jumlah pola tiga digit angka yang muncul adalah "+kata.length+" pola");
        System.out.println();
        System.out.println("SOAL 2");
        for (int i = 0; i < kata.length; i++) {
            int nilai=1;
            for (int j = i + 1; j < kata.length; j++) {
                if(kata[i].equals(kata[j])){
                    kata[j]="null";                    
                    nilai++;                    
                }                
            }
            if(kata[i].equals("null")){

            }else {
                System.out.println("Pola "+kata[i]+" muncul sebanyak "+nilai+" kali");
            }
        }        
    }
}
