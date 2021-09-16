# reverse-of-linkedList-by-using-recursion
reverse of linkedList by using recursion

#include <stdio.h>
#include<stdlib.h>

struct node{
    int data;
    struct node* next;
    
};

void reverse(struct node *ptr){
    if(ptr==NULL)
    return;
    reverse(ptr->next);
    printf("\nafter reverse  ");
    printf("%d ",ptr->data);
}



int main()
{
    int midval=0;
    struct node *head , *first , *second , *third , *fourth , *fifth;
    head = (struct node*) malloc(sizeof(struct node));
    first = (struct node*) malloc(sizeof(struct node));
    second = (struct node*) malloc(sizeof(struct node));
    third = (struct node*) malloc(sizeof(struct node));
    fourth = (struct node*) malloc(sizeof(struct node));
    fifth = (struct node*) malloc(sizeof(struct node));
    
    head->data=1;
    head->next=first;
    
    first->data=2;
    first->next=second;
    
    second->data=3;
    second->next=third;
    
    third->data=4;
    third->next=fourth;
    
    fourth->data=5;
    fourth->next=fifth;
    
    fifth->data=6;
    fifth->next=NULL;
    
    reverse(head);
    
    

    return 0;
}

