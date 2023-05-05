# bst













#include<stdio.h>
#include<stdlib.h>
	struct node 
	{
		struct node *lc;
		int data;
		struct node *rc;
	};
	struct node *root;
	void init()
	{
		root=NULL;
	}
	void bst(int item)
	{
		struct node *t,*t1,*t2;
		t=(struct node *)malloc(sizeof(struct node));
		t->data=item;
		t->RC=NULL;
		t->LC=NULL;

		if(root==NULL)
		{
			root=NULL;
		}
		else
		{
			t1=root;
			while(t!=NULL)
			{
				t1=t2;
				if(item < t1->data)
				{
					t1=t1->LC;
				}
				else
				{
					t1=t1->RC;
				}
			}
			if(item < t2->data)
			{
				t2=RC->t;
			}
			else
			{
				t2=RC->t;
			}
		}
	}
	void inorder(struct node *t)
	{
		if(t!=NULL)
		{
		  inorder(t->LC);
		  printf("%d",t->data);
		  inorder(t->RC);
		}
	}
	void preorder(struct node *t)
	{
		if(t!=NULL)
		{
		  printf("%d",t->data);
		  preorder(t->LC);
		  preorder(t->RC);
		}
	}
	void postorder(struct node *t)
	{
		if(t!=NULL)
		{
		  postorder(t->LC);
		  postorder(t->RC);
		  printf("%d",t->data);
		}
	}
	int main()
	{
	    int i,n,item;
		init();

		printf("\n How many node:::");
		scanf("%d",&n);

		for(i=1;i < n;i++)
		{
			printf("\n Enter the number:::");
			scanf("%d",&item);
			bst(item);
		}
		printf("\n Inorder:::");
		inorder(root);

		printf("\n Preorder:::");
		preorder(root);

		printf("\n postorder:::");
		postorder(root);
	}
