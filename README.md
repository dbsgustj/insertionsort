# insertion-sort
# 설명
자료 배열의 모든 요소를 앞에서부터 차례대로 이미 정렬된 배열 부분과 비교하여,
자신의 위치를 찾아 삽입함으로써 정렬을 완성하는 알고리즘이다.
# 예제
![insertion-sort](https://user-images.githubusercontent.com/126844596/223416052-ea338eac-1370-48b5-ac40-25f8a181adce.png)
# 자바

package test;

public class Insertion_Sort {
	 
	public static void insertion_sort(int[] a) {
		insertion_sort(a, a.length);
	}
	
	private static void insertion_sort(int[] a, int size) {
		
		
		for(int i = 1; i < size; i++) {
			// 타겟 넘버
			int target = a[i];
			
			int j = i - 1;
			
			// 타겟이 이전 원소보다 크기 전 까지 반복
			while(j >= 0 && target < a[j]) {
				a[j + 1] = a[j];	// 이전 원소를 한 칸씩 뒤로 미룬다.
				j--;
			}
			
			/*
			 * 위 반복문에서 탈출 하는 경우 앞의 원소가 타겟보다 작다는 의미이므로
			 * 타겟 원소는 j번째 원소 뒤에 와야한다.
			 * 그러므로 타겟은 j + 1 에 위치하게 된다.
			 */
			a[j + 1] = target;	
		}
		
	}
}
