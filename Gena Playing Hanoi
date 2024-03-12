import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

public class Solution {



    public static void main(String[] args) {

        Scanner scan = new Scanner(System.in);

        int ndisc = scan.nextInt();
        int start = 0;
        for (int h = 1; h <= ndisc; ++h) {
            int rod = scan.nextInt();
            --rod;
            start = move(start, rod, h);

        }
        scan.close();
       
        System.out.print(solve(ndisc, start));
    }

    private static int move(int state, int rod, int disc) {
        return (state & ~(3 << 2 * (disc - 1))) | rod << 2 * (disc - 1);
    }

    private static int getDisc(int ndisc, int state, int rod) {

        int disc = ndisc + 1;
        for (int h = ndisc; h != 0; --h) {
            int r = 3 & state >> 2 * (h - 1);
            if (r == rod) {
                disc = h;
            }
        }
        return disc;
    }

    private static long solve(int ndisc, int start) {
        final int win = 0;
        if (start == win) {
            return 0;
        }
        LinkedList<Integer> bfs = new LinkedList<>();
        bfs.addLast(start);
        List<Integer> depth = Arrays.asList(new Integer[1 << 2 * ndisc]);
        depth.set(start, 0);
        while (true) {
            int par = bfs.getFirst();
            bfs.removeFirst();
            int[] d = new int[4];
            for (int rod = 0; rod < 4; ++rod) {
                d[rod] = getDisc(ndisc, par, rod);
            }
            for (int from = 0; from < 4; ++from) {
                if (d[from] == ndisc + 1) {
                    continue;
                }
                for (int to = 0; to < 4; ++to) {
                    if (d[to] > d[from]) {
                        int ch = move(par, to, d[from]);
                        if (ch == win) {
                            return 1 + depth.get(par);
                        }
                        if (depth.get(ch) == null && ch != start) {
                            depth.set(ch, 1 + depth.get(par));
                                                  
                            bfs.addLast(ch);
                        }
                    }
                }
            }
        }

    }
}
