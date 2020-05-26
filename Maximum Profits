using System;
public class Program {
	public static int MaxProfitWithKTransactions(int[] prices, int k) {
		if((k==0)||(prices.Length==0)){
			return 0;
		}
		int pL = prices.Length;
		int[] oddRow = new int[pL];
		int[] evenRow = new int[pL];
		int[] currentRow = new int[pL];
		int[] previousRow = new int[pL];
		
		for(int t=1;t<k+1;t++){
			int currentMaxPreviousAmount = Int32.MinValue;
			
			if(t%2==1){
				currentRow = oddRow;
				previousRow = evenRow;
			}
			else{
				currentRow = evenRow;
				previousRow = oddRow;
			}
			
			for(int d = 1;d<pL;d++){
				currentMaxPreviousAmount = Math.Max(currentMaxPreviousAmount, previousRow[d-1]-prices[d-1] );
				currentRow[d] = Math.Max(currentRow[d-1], prices[d]+currentMaxPreviousAmount);
			}
			
		
			
			
		}
		
		
		
		int finalVal = k%2==1? oddRow[pL-1]:evenRow[pL-1];
		return finalVal;
	}
}
