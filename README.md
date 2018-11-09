# 11.9.1
前序遍历生成二叉树
// SY1807313_5.cpp : 定义控制台应用程序的入口点。
//

#include "stdafx.h"
#include<stdlib.h>
#include<iostream>
using namespace std;
struct Bitree
{
	int date;
	struct Bitree*LiftTree;
	struct Bitree*RightTree;
};

struct Bitree*Create(void) {//创建一个二叉树
	struct Bitree*q;//创建根节点
	q = (struct Bitree*)malloc(sizeof(struct Bitree));
	int x;
	cin >> x;
	q->date = x;
	if (x == 0) return NULL;
	cout << x << "->LiftTree= ";
	q->LiftTree = Create();
	cout << x << "->RightTree= ";
	q->RightTree = Create();
	return q;
}

int main()
{
	Bitree *Root;
	Root = Create();
    return 0;
}

