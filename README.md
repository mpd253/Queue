# Queue

import java.util.Scanner;
import java.util.Queue;
import java.util.LinkedList;

public class Queue0603 {								// 선입선출 FIFO(First In First Out) Queue

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Queue<Integer> queue = new LinkedList<>();
		Scanner scanner = new Scanner(System.in);
		
		int num = scanner.nextInt();
		
		for(int i = 0; i < num; i++) {
			String some = scanner.next();
			if(some.equals("push")) {
				int somenum = scanner.nextInt();
				queue.offer(somenum);						// stack의 push = queue의 offer
			} else if(some.equals("pop")) {				// 큐에서 가장 위에 있는 정수를 빼고 그 수를 출력
				if(queue.isEmpty()) {
					System.out.println("-1");			// 큐에 들어있는 정수가 없으면 -1을 출력
				} else {				
					System.out.println(queue.poll());	// 큐에 들어있는 정수가 있으면 가장 위에 있는 정수를 빼고 그 수를 출력
				}										// stack의 pop = queue의 poll
			} else if(some.equals("size")) {
				System.out.println(queue.size());		// 큐에 들어있는 정수의 개수를 출력
			} else if(some.equals("empty")) {
				if(queue.isEmpty()) {
					System.out.println("1");			// 큐가 비어있으면 1 출력
				} else {
					System.out.println("0");			// 큐가 비어있지 않으면 0 출력
				}
			} else if(some.equals("front")) {
				if(queue.isEmpty()) {
					System.out.println("-1");			// 큐에 들어있는 정수가 없다면 -1을 출력
				} else {
					System.out.println(queue.peek());	// 큐의 가장 앞에 있는 정수 출력(삭제x)
				}
			} else if(some.equals("back")) {
				if(queue.isEmpty()) {
					System.out.println("-1");			// 큐에 들어있는 정수가 없다면 -1을 출력
				} else {
					System.out.println(?);		// 큐의 가장 뒤에 있는 정수 출력(삭제x)                      - 구현 못했어요!
				}
			}
		}
	}

}
