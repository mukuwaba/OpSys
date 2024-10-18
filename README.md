import static java.lang.Boolean.TRUE;

public class DiningPhilo {
    //Inits

    int i = 0;                                 
    int N = 5;//define N                        //number of philosophers
    int LEFT = (i + N- 1)%N;//define LEFT       //number of i's left neighbor 
    int RIGHT;//define RIGHT                    //number of i's right neighbor 
    int THINKING = 0;//define THINKING          //philosopher is thinking
    int HUNGRY = 1;//define HUNGRY              //philosopher is trying to get forks
    int EATING = 2;//define EATING              //philosopher is eating


    //semaphore mutex = 1                       //mutual exclusion for critical region
    int semaphore;

    //int state[N];                             //array to keep track of everyone's state

    //Create Method's for Philosopher's actions
    public void Think(){
        System.out.println("The philosopher is thinking");


    }//End: Think
    public void Take_forks(){
        System.out.println("The philosopher is thinking");


    }//End: Take_forks
    public void Eat(){
        System.out.println("The philosopher is eating");


    }//End: Eat
    public void Put_forks(){
        System.out.println("The philosopher is placing forks");


    }//End: put_forks

    //i: philosopher number, from 0 to N - 1
    public void philosopher(int i) {
        while (TRUE) { //repeat forever
            Think(); //philosopher is thinking
            Take_forks(); //acquire two forks or block
            Eat();// eat spaghetti
            Put_forks(); //put both forks back on table
        }//End: while

    }//End: philosopher

    //i: philosopher number, from 0 to N - 1
    public static void take_forks(int i) {
        //down(&mutex);         //enter critical region
        //state[i] = HUNGRY;    //record fact that philosopher is hungry
        //test(i)               //try to acquire two forks
        //up(&mutex)            //exit critical region
        //down(&s[i]);          //block if forks were not aquired
    }//End: take_forks

    //i: philosopher number, from 0 to N - 1
    public static void put_forks(int i) {
        //down(&mutex);         //enter critical region
        //state[i] = THINKING   //philosopher has finished eating
        //test(LEFT)            //see if left neighbor can eat now
        //test(RIGHT)           //see if right neighbor can eat now
        //up(&mutex)            //exit critical region
    }//End: put_forks

    //i: philosopher number, from 0 to N - 1
    public static void test(int i){
        //if(state[int i]==HUNGRY && state[LEFT] != EATING && state[RIGHT] !=EATING){
            //state[i] = EATING;
            //up(&s[i]);

    }//End: test
}//End: DiningPhilo




