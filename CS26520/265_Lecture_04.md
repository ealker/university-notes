# CS26520 Lecture 4
## Propositional Logic
__Monday, February 5th 2018__  
Lecture: mxw@aber.ac.uk   
Notes: ela12@aber.ac.uk  

These notes are based off of the course notes provided by [Dr. Myra Wilson](https://www.aber.ac.uk/en/cs/staff-list/staff_profiles/?staff_id=mxw).

## Syntax  

The syntax of propositonal logic defines allowable sentence within the logic. 

- **Atomic sentences** consist of a single proposition symbol. This captures the truth behind a statement. 
    - Each proposition symbol starts with an uppercase letter. 
    - Names are arbitrary. 
    - W, Q, North, etc.
- Each proposition can either be **true** or **false**.
    - A proposition cannot be both true and false. 
- The following are examples of propositions: 
    - John is a boy. 
    - Elliot is 19. 

Complex sentences are constructed from simple sentences and make use of **logical connectives**. The truth value of a complex sentence depends upon the truth value of the sentence's components and the operations defines by the logical connectives used. The following are the logical connectives in order of precendence:

- &not; (Negation) Inverts the truth of a term.
    - &not;Q is the inverstion of Q. 
    - Positive literal = atomic sentence. 
    - Negative liveral = negated atomic sentence. 
- &and; (Conjunction) Requires both conjoined terms to be true for the whole conjunction to be true. 
    - Parts of the sentence are called the conjuncts.
- &or; (Disjunction) Only requires one term to be true for the whole disjunction to be true.
    - Parts of the sentence are called the disjuncts.
    - &or; comes from the Latin 'vel' meaning 'or'.
- $\Rightarrow$ (Implication) True if the antecedents (premise) are true while the
consequents are true. Also true when the antecedents are false.  
    - P $\Rightarrow$ Q 
        - “if P is true then Q is true, otherwise I am making no claim”. 
        - If that's satisfied then the implication is true.
    - Also called a conditional.
    - Also called 'if-then' statements.
- $\Leftrightarrow$ (Equivalency) The terms are equivalent. 
    - "If and only if".

**Tip:** One can determine if a statement is a proposition by prefixing it with “Is it true that.....” and seeing if it makes grammatical sense.

### Backus-Naur Form Grammar of Propositional Logic Sentences 

![BNF Grammer of PL Sentences](\265_img\26504_bnf.png)

## Semantics 

The semantics of propositonal logic define the rules for determining the truth of a given sentence with respect to a particular model. Propositional logic simply assigns a truth value for every propositional symbol in a sentence. 

Example: 

The propositional symbols, $P_{1,2}, P_{2,2}, P_{3,1}$, could have the following model:

$m_{1} = \{P_{1,2} = false, P_{2,2} = false, P_{3,1} = true\}$. 

"The semantics for propositional logic must specify how to compute the truth value of any sentence given a model, which is done recursively. Any sentence in PL is constructed from atomic sentences and the five logical connectives. 

- Atomic Sentences: 
    - $True$ is true in every model.
    - $False$ is false in every model.
    - Truth value of every other propsition is specified in the model. 
- Complex Sentences: 

### Truth Tables 
![BNF Grammer of PL Sentences](\265_img\26504_tt.png)

