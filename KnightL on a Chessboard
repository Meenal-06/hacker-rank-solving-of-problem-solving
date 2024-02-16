import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {
    
    static class Point {
        int x;
        int y;
        int turn;
        Point(int x,  int y, int turn) {
            this.x = x;
            this.y = y;
            this.turn = turn;
        }
           
    }

    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int n = in.nextInt();
        
        int[][] result = new int[n][n];
        for (int a = 1; a < n; a++) {
            for (int b = 1; b < n; b++) {
                if (result[b][a] != 0) {
                    System.out.print(result[b][a]);
                    if (b < n - 1) 
                        System.out.print(" ");
                } else {
                boolean[][] visited = new boolean[n][n];
                Queue<Point> queue = new LinkedList<>();
                queue.add(new Point(0, 0, 0));
                visited[0][0] = true;
                
                boolean hit = false;
                while (!queue.isEmpty()) {
                    Point pt = queue.poll();
                    
                    int x = pt.x - a;
                    int y = pt.y - b;
                    if (x >= 0 && y >= 0 && !visited[x][y]) {
                        if (x == n - 1 && y == n - 1) {
                            System.out.print(pt.turn + 1);
                            hit = true;
                            result[a][b] = pt.turn + 1;
                            if (b < n - 1)
                                System.out.print(" ");
                            break;
                        } else {
                            visited[x][y] = true;
                            queue.add(new Point(x, y, pt.turn + 1));
                        }
                    }
                    
                    x = pt.x + a;
                    y = pt.y - b;
                    if (x < n && y >= 0 && !visited[x][y]) {
                        if (x == n - 1 && y == n - 1) {
                            System.out.print(pt.turn + 1);
                            hit = true;
                            result[a][b] = pt.turn + 1;
                            if (b < n - 1)
                                System.out.print(" ");
                            break;
                        } else {
                            visited[x][y] = true;
                            queue.add(new Point(x, y, pt.turn + 1));
                        }
                    }
                    
                    x = pt.x - a;
                    y = pt.y + b;
                    if (x >= 0 && y < n && !visited[x][y]) {
                        if (x == n - 1 && y == n - 1) {
                            System.out.print(pt.turn + 1);
                            hit = true;
                            result[a][b] = pt.turn + 1;
                            if (b < n - 1)
                                System.out.print(" ");
                            break;
                        } else {
                            visited[x][y] = true;
                            queue.add(new Point(x, y, pt.turn + 1));
                        }
                    }
                    
                    x = pt.x + a;
                    y = pt.y + b;
                    if (x < n && y < n && !visited[x][y]) {
                        if (x == n - 1 && y == n - 1) {
                            System.out.print(pt.turn + 1);
                            hit = true;
                            result[a][b] = pt.turn + 1;
                            if (b < n - 1)
                                System.out.print(" ");
                            break;
                        } else {
                            visited[x][y] = true;
                            queue.add(new Point(x, y, pt.turn + 1));
                        }
                    }
                    
                    x = pt.x - b;
                    y = pt.y - a;
                    if (x >= 0 && y >= 0 && !visited[x][y]) {
                        if (x == n - 1 && y == n - 1) {
                            System.out.print(pt.turn + 1);
                            hit = true;
                            result[a][b] = pt.turn + 1;
                            if (b < n - 1)
                                System.out.print(" ");
                            break;
                        } else {
                            visited[x][y] = true;
                            queue.add(new Point(x, y, pt.turn + 1));
                        }
                    }
                    
                    x = pt.x + b;
                    y = pt.y - a;
                    if (x < n && y >= 0 && !visited[x][y]) {
                        if (x == n - 1 && y == n - 1) {
                            System.out.print(pt.turn + 1);
                            hit = true;
                            result[a][b] = pt.turn + 1;
                            if (b < n - 1)
                                System.out.print(" ");
                            break;
                        } else {
                            visited[x][y] = true;
                            queue.add(new Point(x, y, pt.turn + 1));
                        }
                    }
                    
                    x = pt.x - b;
                    y = pt.y + a;
                    if (x >= 0 && y < n && !visited[x][y]) {
                        if (x == n - 1 && y == n - 1) {
                            System.out.print(pt.turn + 1);
                            hit = true;
                            result[a][b] = pt.turn + 1;
                            if (b < n - 1)
                                System.out.print(" ");
                            break;
                        } else {
                            visited[x][y] = true;
                            queue.add(new Point(x, y, pt.turn + 1));
                        }
                    }
                    
                    x = pt.x + b;
                    y = pt.y + a;
                    if (x < n && y < n && !visited[x][y]) {
                        if (x == n - 1 && y == n - 1) {
                            System.out.print(pt.turn + 1);
                            hit = true;
                            result[a][b] = pt.turn + 1;
                            if (b < n - 1)
                                System.out.print(" ");
                            break;
                        } else {
                            visited[x][y] = true;
                            queue.add(new Point(x, y, pt.turn + 1));
                        }
                    }
                }
                if (!hit) {
                    result[a][b] = -1;
                    System.out.print("-1");
                    if (b < n - 1)
                        System.out.print(" ");                
                }
                }
            }
            if (a < n - 1) {
                System.out.println();
            }
        }
    }
}

