public class GnomeSort {


    public static void sort(int[] array) {
        int index = 0;
        int comparacoes = 0; // Contador de comparações
        int trocas = 0;      // Contador de trocas

        while (index < array.length) {
            if (index == 0 || array[index] >= array[index - 1]) {
                comparacoes++; // Comparação bem-sucedida
                index++;
            } else {
                
                int temp = array[index];
                array[index] = array[index - 1];
                array[index - 1] = temp;
                trocas++; 
                index--;
            }
        }

        
        System.out.println("Comparações realizadas: " + comparacoes);
        System.out.println("Trocas realizadas: " + trocas);
    }

    
    public static void main(String[] args) {
        int[] data = {34, 2, 78, 12, 45, 67, 1, 89};
        
        System.out.println("Array antes da ordenação:");
        for (int num : data) {
            System.out.print(num + " ");
        }

       
        sort(data);

        System.out.println("\n\nArray após a ordenação:");
        for (int num : data) {
            System.out.print(num + " ");
        }
    }
}
