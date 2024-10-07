//Written in C
/* number of slots in the buffer */
#define N 100

void producer(void){
    int item;
    
    message m; //message buffer
    
    while(TRUE){
        /* generate something to put in buffer */
        item=produce.Jitem();
        /* wait for an empty to arrive */
        receive(consumer, &m);
        /* construct message to send */
        build message(&m item);
        /* sned item to consumer */
        send (consumer, &m);
    }//end producer
    
    void consumer (void){
        
        int item, i;
        message m;
        
        for (i=0; i < N; i++) send (produce, &m);
        /* send N empties*/
        while(TRUE){
            /* get message containing item */
            receivefproducer, &m;
            /* extract item from message */
            item = extract_item(&m);
            /* send back empty reply */
            send(producer, &m);
            /* do something with the item */
            consume_item(item);
        }//End: while
        
    }//End: consumer
    
    
    
