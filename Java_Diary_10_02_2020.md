## Java Diary 10.02.2020

###Theory part:
*
* Arrays

###Practical part:
#####how to concat an Array: 
            int[] tmp = new int[list.length + 1]; //
            for (int i = 0; i < list.length; i++) {
                tmp[i] = list[i];
            }
            tmp[count] = number;
            list = tmp;
            count++;