# Korea University Conditioning Simulator (KUCS)

[Go to Release Page](https://github.com/knowblesse/Modeling/releases/tag/v1.3)


# Manual
[Download the Manual](https://github.com/knowblesse/Modeling/blob/main/KUCS/KUCS/KUCS_Doc.pdf)

# Change Log
### v1.3 :
- [Changed] **Project renamed : Korea University Conditioning Simulator**
- [Changed] model notation is improved. (does not effect the script)
    - Program's equation image is updated
- [Changed] Graph drawing speed is significantly increased in some devices (drawing time reduced 80%)
    - I don't know why, but legend function was consuming a lot of time. (preallocation problem?)

### v1.2.1 :
- [Changed] SPH model doesn't update alpha if the corresponding CS is not presented.
    - The original thesis does not clearly specify this in the equation.
    - However, if this rule is not applied to the alpha updating rule, all alpha values remain the same across CSs. 

### v1.2 :
- [Fixed] Pearce-Hall model error fixed (I'm keep writing it as "Pearson-Hall")
- [Changed] Default model parameter changed

### v1.1 : 
- [Fixed] weight is now initialized everytime the simulation is performed.
- [Changed] Since the initial alpha values are presented in the 'Stage Configuration' panel, now, it's not presented in the 'Experiment Schedule' panel.
- [Changed] Experiment Schedule notation changed. 
	- Deleted alpha values
	- No US is now encoded as '-'
	- Experiment schedule parsing method is also changed.
- [Changed] Mackintosh model is changed into the new form. 
	- applyed (1-a) and (a) term in the delta alpha. This smooths the increase/decrase curve and automatically limits the alpha in [0,1].
	- New equation is similar to the formalization of Moore & Stickney(1975).
	- But it uses small negative number 'epsilon' when the discrepancy of the CS and X are equal. 
	- This change allows the model to successfully predict Latent Inhibition.
- [Changed] All Experiment Template were changed to have initial alpha value of 0.5. (Previously, there were two options).

### v1.0 : 29114a
Initial working version


