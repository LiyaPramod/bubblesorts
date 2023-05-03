import java.util.Scanner;
  class Source {
   static int totalBubbleSortSwaps(int[] array, int M) {
       int size = array.length;
       int var = 0;
       int totalSwaps = 0;
       for(int i =0;i<M;i++)
       {
           boolean swapped = false;
           for(int j=0;j<size-1;j++){
               if(array[j]<array[j+1])
               {
                   int temp=array[j];
                   array[j]=array[j+1];
                   array[j+1]=temp;
                   totalSwaps++;
                   swapped=true;
               }
           }
           if(!swapped)
           {
               break;
           }
       }
       return totalSwaps;
   }
   public static void main(String args[])
   {
       Scanner scanner = new Scanner(System.in);
       int M = scanner.nextInt();
        int n = scanner.nextInt();
        int[] array = new int[n];
        for (int i = 0; i < n; i++) {
            array[i] = scanner.nextInt();
        }
            int totalSwaps = totalBubbleSortSwaps(array, M);
            System.out.println(+totalSwaps);

        
   }
}
