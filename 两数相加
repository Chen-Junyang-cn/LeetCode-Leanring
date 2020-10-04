/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode() : val(0), next(nullptr) {}
 *     ListNode(int x) : val(x), next(nullptr) {}
 *     ListNode(int x, ListNode *next) : val(x), next(next) {}
 * };
 */
class Solution {
public:
    ListNode* addTwoNumbers(ListNode* l1, ListNode* l2) {
        ListNode* head = new ListNode(-1);
        ListNode* tail = head;
        int carry = 0;
        while (l1 || l2) {
            int n1 = l1 ? l1->val : 0;
            int n2 = l2 ? l2->val : 0;
            int sum = n1 + n2 + carry;
            carry = sum / 10;
            tail->next = new ListNode(sum % 10);
            tail = tail->next;
            if (l1) l1 = l1->next;
            if (l2) l2 = l2->next;
        }
        if (carry)  tail->next = new ListNode(1);
        return head->next;
    }
};
/*int num = l1->val + l2->val;
        int carry = 0;
        if (num >= 10) {
            num %= 10;
            carry = 1;
        }
        ListNode* head = new ListNode(num);
        l1 = l1->next, l2 = l2->next;
        ListNode* res = head;
        while (l1 && l2) {
            num = l1->val + l2->val + carry;
            carry = 0;
            if (num >= 10) {
            num %= 10;
            carry = 1;
            }
            ListNode* sum = new ListNode(num);
            res->next = sum;
            l1 = l1->next, l2 = l2->next;
            res = sum;
        }
        while (l1) {
            num = l1->val+ carry;
            carry = 0;
            if (num >= 10) {
            num %= 10;
            carry = 1;
            }
            ListNode* sum = new ListNode(num);
            res->next = sum;
            l1 = l1->next;
            res = sum;
        }
        while (l2) {
            num = l2->val + carry;
            carry = 0;
            if (num >= 10) {
            num %= 10;
            carry = 1;
            }
            ListNode* sum = new ListNode(num);
            res->next = sum;
            l2 = l2->next;
            res = sum;
        }
        if (carry == 1) {
            ListNode* sum = new ListNode(1);
            res->next = sum;
        }
        return head;*/
