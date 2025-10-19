# README

---

# D.S-Assignment

## Linked List Team Project – `<codeconnectors>`
README
---

##  Overview

This project is part of *CO3 – Data Structures Lab (S3, INMCA2024-29)*.
It demonstrates:

* ✅ Implementation of a **Singly Linked List** in C
* ✅ Collaborative development using **GitHub** (branches, commits, pull requests)
* ✅ Visualization of linked list operations using **Figma**
* ✅ Team collaboration & reporting

---

##  Singly Linked List Program

The C program creates a singly linked list using integer roll numbers.
It supports:

* Insertion at the end
* Traversal to display roll numbers in order

---

### ✅ Code Snippet

```c
#include <stdio.h>
#include <stdlib.h>
struct Node{
    int rollNumber;
    struct Node* next;
};
struct Node* createNode(int rollNumber){
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->rollNumber = rollNumber;
    newNode->next = NULL;
    return newNode;
}
void insertNode(struct Node** head, int rollNumber){
    struct Node* newNode = createNode(rollNumber);
    if (*head == NULL){
        *head = newNode;
        return;
    }
    struct Node* temp = *head;
    while (temp->next != NULL){
        temp = temp->next;
    }
    temp->next = newNode;
}
void displayList(struct Node* head){
    struct Node* temp = head;
    printf("Roll Numbers in Linked List:");

    while (temp != NULL){
        printf("%d", temp->rollNumber);
        if (temp->next != NULL){
            printf(" -> ");
        }
        temp = temp->next;
    }

    printf("\n");
}
int main(){
    struct Node* head = NULL;
    insertNode(&head, 24);
    insertNode(&head, 29);
    insertNode(&head, 39);
    insertNode(&head, 52);
    displayList(head);
    return 0;
}
```

---

###  Sample Output

```
Roll Numbers in Linked List : 24 -> 29 -> 39 -> 52
```

---

 Team Workflow — Single Linked List Project
 Development Strategy

The team adopted a modular development approach, where each contributor focused on an isolated module (e.g., insertion, deletion, traversal). This allowed parallel development and reduced merge conflicts.

Branches were named to reflect both the feature and contributor for better traceability:

feature/<function>-<name>


Examples:

feature/insert-middle-mariya

feature/display-fasila

feature/delete-value-devanandha

feature/search-sara

This naming convention ensured better accountability and simplified PR tracking.

 Task Allocation

Tasks were divided based on core functionalities of singly linked lists, with some members also handling cross-functional responsibilities:

Node management & memory allocation

Insertion operations (beginning, specific position, end)

Deletion operations (by value, by position)

Traversal and display

Reversing the list

Search functionality

Calculating list length

Code cleanup and error handling

In addition, team roles included documentation, code review, and GitHub workflow coordination.

 Contribution Workflow

To ensure consistency and smooth collaboration, the following Git-based workflow was followed:

Sync with the main branch:

git pull origin main


Create a new feature branch:

git checkout -b feature/<function>-<your-name>


Implement and test the assigned module locally.

Commit with a descriptive message:

git commit -m "Add <function> functionality to linked list"


Push the branch to GitHub:

git push origin feature/<function>-<your-name>


Open a Pull Request (PR) and assign reviewers.

Collaborate on code reviews, address feedback, and resolve conflicts.

Once approved, the branch was merged into main.

 Testing & Validation

Each function was unit-tested independently for correctness.

Post-merge, the entire linked list program was tested as an integrated system.

Special attention was given to edge cases such as:

Inserting into an empty list

Deleting the only node

Searching for non-existent values

Memory management and pointer safety were verified to prevent leaks and crashes.

##  Figma Diagram

###  Purpose:

To visually represent:

* **Node structure** (`data`, `next`)
* **Insertion logic** (sequential linking)
* **Traversal flow**

###  Diagram Preview:

![Figma Diagram](https://github.com/fasilasathar/linked-list/blob/main/29%2039%2052%2024.png)

###  Public Figma Link:

[Click here to view in Figma](https://www.figma.com/design/MQY2hudHYceVL7jgJ4UWUP/Untitled?node-id=0-1&p=f&t=itOqAj1MgsiVVFul-0)

---

##  Final Report

The final report includes:

* ✅ Figma Diagram + Screenshot

* ✅ Final working code + output

* ✅ Contributions + Reflection

* 📄 [Download Report (PDF)](https://github.com/fasilasathar/linked-list/blob/main/Report%20Final%2024%2029%2039%2052.pdf)

---

##  Team Contributions

| Member         | Roll No | GitHub Contribution                              |
| -------------- | ------- | ------------------------------------------------ |
| Fasila Sathar  | 29      | Created repository structure + Managed issues    |
| Mariya Joseph  | 39      | Implemented CI workflows + Branch protection     |
| Devanandha P S | 24      | Designed README.md + Added project wiki pages    |
| Sara Paul      | 52      | Reviewed PRs + Managed labels & milestones       |

---

 Reflection

    ⦾ Grasped the concept of node-based memory allocation and how pointers link data in C

    ⦾ Implemented and debugged multiple insertion scenarios to strengthen problem-solving skills

    ⦾ Explored the workflow of open-source collaboration through GitHub commits and pull reviews

    ⦾ Created clean and readable documentation using Markdown and collaborative tools

    ⦾ Learned to plan and divide tasks efficiently within the team using milestones and issue tracking
