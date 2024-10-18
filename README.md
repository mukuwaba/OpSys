import static java.lang.Boolean.TRUE;

public class DiningPhilo {
    //Inits

    int i = 0;
    int N = 5;//define N
    int LEFT = (i + N- 1)%N;//define LEFT
    int RIGHT;//define RIGHT
    int THINKING = 0;//define THINKING
    int HUNGRY = 1;//define HUNGRY
    int EATING = 2;//define EATING


    //semaphore mutex = 1
    int semaphore;

    int state = N;

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
        //down(&mutex);
        //state[i] = THINKING
        //test(LEFT)
        //test(RIGHT)
        //up(&mutex)
    }//End: put_forks

    //i: philosopher number, from 0 to N - 1
    public static void test(int i){
        //if(state[int i]==HUNGRY && state[LEFT] != EATING && state[RIGHT] !=EATING){
            //state[i] = EATING;
            //up(&s[i]);

    }//End: test
}//End: DiningPhilo




