  

## 선형 배열

![[Untitled 6.png|Untitled 6.png]]

그림 출처: [https://www.geeksforgeeks.org/array-data-structure/?ref=shm](https://www.geeksforgeeks.org/array-data-structure/?ref=shm)

  

선형 자료구조다. 동일한 타입의 데이터를 연속적으로 저장하고, 그러므로 관리하기가 쉽다. 가장 기본적인 자료구조다.

배열에는 index가 있는데, 이는 방 번호라고 생각하면 된다.

element는 각 방에 있는 요소의 값이다.

위 그림의 표에 따르면 0번 방엔 Array[0] = 2가 있는 것이다.

  

- 배열 코드 예시
    
    ```Java
    	public static void main(String[] args) {
    		// 1차원 배열 선언(객체 생성)
    		int[] arr1 = new int[] {1, 2, 3, 4, 5};
    		int[] arr2 = new int[4];
    		//for문을 통해 값 삽입
    		for (int i = 0; i < arr2.length; i++)
    			arr2[i]= i;
    		//for문을 통해 출력
    		for (int i = 0; i < arr1.length; i++) 
    			System.out.print(arr1[i]+ " ");
    		System.out.println();
    
    		//Arrays.toString을 통해 출력
    		System.out.println(Arrays.toString(arr2));
    		
    		// 기존의 연결을 끊고 새로운 객체 생성
    		arr2 = new int[] {1, 3, 5, 7, 9};
    		//foreach문을 통해 출력
    		for(int num : arr2)
    			System.out.printf("%d ", num);
    		System.out.println();
    		
    		//2차원 배열 선언(객체 생성)
    		int[][] arr3 = new int[][] {{1, 2}, {3, 4}};
    		int[][] arr4 = new int[2][2];
    		//이중 for문을 통해 값 삽입
    		for (int i= 0; i < arr4.length; i++) 
    			for (int j = 0; j < arr4[i].length; j++)
    				arr4[i][j] = 10 * i + j; 
    		//이중 foreach 문을 통해 출력
    		for (int[] newArr : arr3) {
    			for (int num : newArr) {
    				System.out.print(num+" ");
    			}
    			System.out.println();
    		}
    		//2차원 배열을 Arrays.toString을 사용하면 주소값을 출력한다.
    		System.out.println(Arrays.toString(arr4));
    		//2차원 배열을 출력할 땐 Arrays.deepToString 사용.
    		System.out.println(Arrays.deepToString(arr4));
    	}
    ```
    
    [0, 1, 2, 3]  
    1 3 5 7 9  
    1 2  
    3 4  
    [[I@35851384, [I@649d209a]  
    [[0, 1], [10, 11]]  
    
      
    
      
    

  

## 다차원 배열

![[Untitled 1 3.png|Untitled 1 3.png]]

  

보통 3차원 배열 이상은 사용하지 않는다.

  

- 다차원 배열 코드 예시
    
    ```Java
    public class Matrix {
        public static void main(String[] args) {
            //다차원 배열 선언
            int[][] matrix1 = new int[3][3];
            int[][] matrix2 = new int[][]{{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
    
            for (int i = 0; i < matrix2.length; i++) {
                for (int j = 0; j < matrix2[0].length; j++) {
                    System.out.print(matrix2[i][j] + " ");
                }
                System.out.println();
            }
        }
    }
    ```
    

  

[[복사]]