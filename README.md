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

    
    public void philosopher(int i) {
        while (TRUE) {
            Think();
            Take_forks();
            Eat();
            Put_forks();
        }//End: while

    }//End: philosopher
    
    public static void take_forks(int i) {
        //down(&mutex);
        //state[i] = HUNGRY;
        //test(i)
        //up(&mutex)
        //down(&s[i]);
    }//End: take_forks
    
    public static void put_forks(int i) {
        //down(&mutex);
        //state[i] = THINKING
        //test(LEFT)
        //test(RIGHT)
        //up(&mutex)
    }//End: put_forks
    
    public static void test(int i){
        //if(state[int i]==HUNGRY && state[LEFT] != EATING && state[RIGHT] !=EATING){
            //state[i] = EATING;
            //up(&s[i]);
        
    }//End: test
}//End: DiningPhilo




