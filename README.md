# boston-regression
ML Project #2: Running through the Boston dataset and getting some hands-on experience with sci-kit learn.

### What was new:
* Touched on `GridSearchCV` and hyperparameter-tuning in general.
* Had a more organized flow of methodology and a clear approach in my mind of what needs to be done.
* Did a stratified `train_test_split`, based on the most correlated independent variable `LSTAT`.
* Messed around with `pickle` for ease of saving and transferring train/test data.
* Created Polynomial Features on `CRIM` and `B` because they seemed a little non-linear. Will go back and do it on `LSTAT`.
* Created a (semi-)functional custom transformer for `ZN`. Will need to try give it `get_feature_names_out()` method.
* After applying preprocessing, I did simple model `.fit` & `.predict` to get accuracy to see if I am going in the right direction. Also, tested against a simple benchmark predictor.

### What questions did I raise for myself that are yet to be answered:
* How to remove or avoid reproduction of data quirks in data? For example, `AGE` column seemed to be maxed out at 100 years, so there was a solid vertical line if one looks at scatter plot of `AGE` and `MEDV` - what is known as Boundary Effect.
* How to choose a correct Feature Transformation? Is it even important?
  * I still don't know how it is for the first question, but something tells me it is a trial and error process.
  * As per importance, I understood it is **required** for a linear model, while for other models like Gradient Descent it is merely beneficial because it improves the score. Tree-based models actually fared-well even with `basic_preprocessing` - why?

### What I want to try next:
* More extensive model validation and testing - I feel like `learnin_curves` would be great in visualizing performance.

### Takeaways:
- Create more visuals for inspecting performance (**matplotlib**).
- Tinker more with **`sklearn`**'s transformers.
- Learn more about **Feature Engineering** (Selection/Transformation/Scaling).
