# #include <stdio.h>
#include<stdlib.h>
struct node{
    int data;
    struct node *next;
    
};
void create(struct *head){
    struct*newnode,*ptr;
    int num;
    printf("enter -1 to end/n");
    printf("enter the data");
    scanf("%d",&num);
    while(num!=-1){
        newnode=(struct node*) malloc(sizeof(struct node));
        newnode->data=NULL;
        newnode->next=NULL;
        if(head==NULL){
        head=newnode;    
        }else
        ptr=head;
        while(head->next!=NULL){
            ptr=ptr->next;
        }
    }
}


int main() {
int choice;
struct node *head =NULL;
do{
    printf("head");
printf("enter choice");
scanf("%d", choice);

    switch(choice){
        case 1:
        create(&head);
        break;
        case 2:
        insertf(&head);
        break;
         case 3:
        insertend(&head);
        break;
         case 4:
        insertanywhere(&head);
        break;
         case 5:
        display(&head);
        break;
    }
}
while(choice!=0);

    return 0;
}
