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


    }//End: Take_forks
    public void Eat(){


    }//End: Eat
    public void put_forks(){


    }//End: put_forks

    public void philosopher(){


    }



}//End: class_Dining Philo


