# InputArray

import java.util.Arrays;
import java.util.HashMap;
import java.util.Scanner;

public class InputArray {

        public int[] twoSum(int[] numbers, int target) {
            int[] result = new int[2];
            HashMap<Integer, Integer> hash = new HashMap<>();

            for(int i=0; i<numbers.length;i++){
                if(hash.containsKey(target - numbers[i])){
                    result[1] = i;
                    result[0] = hash.get(target - numbers[i]);
                }
                hash.put(numbers[i],i);
            }
            return result;

        }
        public void imprimir(int[] numbers, int target){
            System.out.println(Arrays.toString(numbers));
            System.out.println("El resultado es: " + Arrays.toString(twoSum(numbers, target)) );
        }



    public static void main(String[] args) {
            InputArray array = new InputArray();
            Scanner sca = new Scanner(System.in);
            int[] num = new int[4];
            int target = 9;

        for(int i = 0; i < num.length; i++){
            num[i] = sca.nextInt();
        }
        array.imprimir(num,target);
    }
    }

