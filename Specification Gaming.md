[Specification Gaming](https://deepmind.google/discover/blog/specification-gaming-the-flip-side-of-ai-ingenuity/) is the behaviour of satisfying the specification of an objective without actually completing the intended task 

<span style="color:aquamarine">Cheating or finding shortcuts</span> is a good and simple example of this in real life

### Why does this happen?
1. **Misspecification** - This isn't a flaw in the RL algorithm. Rather, it's because **the objective itself is not specified correctly** 
2. **Poorly designed reward shaping** - Shaping rewards can change the *optimal policy*, sometimes for the worse. This happens when they're not *potential-based*
3. **Incorrect assumptions** - A common form of incorrect assumptions is that agents cannot exploit bugs that are exposed during simulations in the real world. This is a problem especially when designers _consider the specified tasks to be immune to tampering_ -> **Reward tampering problem**
4. 
>[!Note]
>Specification gaming, while usually thought as unintended or bad, can actually be a **good sign** in *some cases*. Such behaviours may **encourage the system to learn novel and innovate methods to achieve the objective**. After all, there can be multiple solutions to a given problem

**Task Specification** - Reward function design, training environments, auxiliary rewards etc. More of a catch-all term

**Correctness of task specification <--> Intended outcome** 

### Challenges summarized
* How do we avoid reward tampering?
* How do we faithfully capture human concepts?
* How do we avoid making incorrect assumptions?
### Important Takeaways
1. Always try to **properly specify the intent**
2. A combination of **RL Algorithm Design** and **Reward Design** is crucial
3. Don't try to cover every possible case while specifying - **Learn the reward function from human feedback**

