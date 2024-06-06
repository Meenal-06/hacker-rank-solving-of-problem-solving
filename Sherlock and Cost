import java.io.*;
import java.util.*;

public class Solution 
{

    public static void main(String[] args) 
    {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */
        Scanner scanner = new Scanner(System.in);
        int T = scanner.nextInt();
        
        while (T > 0)
        {
            int N = scanner.nextInt();
            int length = N;
            int inputArray[] = new int[length];
            for(int i=0; i<N; i++)
            {
                inputArray[i] = scanner.nextInt();     
            }
            int dp[][] = new int[N][2];
            dp[0][0]=0;
            dp[0][1]=0;
            for(int i=1; i<N; i++)
            {
                dp[i][0] = Math.max(dp[i-1][0],dp[i-1][1] + inputArray[i-1] - 1);
                dp[i][1] = Math.max(dp[i-1][1], dp[i-1][0] + inputArray[i] -1);
            }
            System.out.println(Math.max(dp[N-1][0], dp[N-1][1]));
            T--;
        }
    }
}
