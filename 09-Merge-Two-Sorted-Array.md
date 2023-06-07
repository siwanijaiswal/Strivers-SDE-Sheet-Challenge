 ## [Merge Two Sorted Array](https://www.codingninjas.com/codestudio/problems/merge-two-sorted-arrays_8230835?challengeSlug=striver-sde-challenge&leftPanelTab=1)




```Optimal Approach```
 ```cpp
#include <bits/stdc++.h>

vector<int> ninjaAndSortedArrays(vector<int>& arr1, vector<int>& arr2, int m, int n) {
	// we will start from the end of the two arrays and will compare the elements and will place them at the end of the first array
	int i = m-1, j = n-1, k = m+n-1;

	while(i >= 0 and j >= 0){
		if(arr2[j] > arr1[i]){ 
			// if the element of the second array is greater than the element of the first array then place the element of the second array at the end of the first array
			arr1[k--] = arr2[j--]; 
		} else {
			// if the element of the first array is greater than the element of the second array then place the element of the first array at the end of the first array
			arr1[k--] = arr1[i--];
		}
	} 

	// if there are still some elements left in the second array then place them at the end of the first array, this case will occur when elements of the second array is greater than the elements of the first array
	while(j >= 0) arr1[k--] = arr2[j--];

	return arr1;

	/*
	TC: O(m+n)
	SC: O(1)
	*/
}
``` ## [Merge Two Sorted Array](https://www.codingninjas.com/codestudio/problems/merge-two-sorted-arrays_8230835?challengeSlug=striver-sde-challenge&leftPanelTab=1)




```Optimal Approach```
 ```cpp
#include <bits/stdc++.h>

vector<int> ninjaAndSortedArrays(vector<int>& arr1, vector<int>& arr2, int m, int n) {
	// we will start from the end of the two arrays and will compare the elements and will place them at the end of the first array
	int i = m-1, j = n-1, k = m+n-1;

	while(i >= 0 and j >= 0){
		if(arr2[j] > arr1[i]){ 
			// if the element of the second array is greater than the element of the first array then place the element of the second array at the end of the first array
			arr1[k--] = arr2[j--]; 
		} else {
			// if the element of the first array is greater than the element of the second array then place the element of the first array at the end of the first array
			arr1[k--] = arr1[i--];
		}
	} 

	// if there are still some elements left in the second array then place them at the end of the first array, this case will occur when elements of the second array is greater than the elements of the first array
	while(j >= 0) arr1[k--] = arr2[j--];

	return arr1;

	/*
	TC: O(m+n)
	SC: O(1)
	*/
}
```