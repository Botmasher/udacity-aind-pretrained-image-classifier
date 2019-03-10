# Project: Use a Pre-Trained Image Classifier

## 1. Instructor
- lab by statistician and comp scientist from FL Poly

## 2. Project Description
- goal is to improve programming with Python, so focus on that
- participants in a city dog show submit image, bio of their dog
- some participants intend to register non-dogs
- use an already created classifier to tell dogs from non-dogs
- results: "dogs", "not dogs"
- determine which algorithm does the best at determining dog/non-dog
- consider time vs accuracy
- use a CNN (CNNs are good with image features like color, edge, texture)
- the CNN is already trained on 1.2 million images
- compare 3 architectures for best fit: AlexNet, VGG, ResNet
- amount of data for similar breeds helps classify them apart

## 3. Project Instructions
- objectives:
    - which images are dogs vs not dogs?
    - what is the breed of the dog images?
    - which CNN model best achieves the above?
    - would another solution be good enough considering time?
- edit `check_images.py`
- consult `_hints.py` if you're struggling
- consult [project FAQ](https://github.com/udacity/AIPND-revision/blob/master/notes/project_intro-to-python.md)
- docstrings provide guidance on input and output
- the rest of these notes below help build out undefined functions

## 4. Workspace
- description of how to use the udacity terminal + file tree + editor workspace
- NOTE: I `conda` installed pytorch; setup ran when I `python`ed the test file

## 5. Timing Code
- look at `check_images.py` and fill out name, date
- get `time()` and `sleep()` from the Python `time` module
- time the code in `main()` using the functions

## 6. (Workspace)
- test out timing

## 7. Command Line Arguments
- use argparse to get 3 command line args from user
- fill out `get_input_args.py`
- `check_command_line_arguments` tests it
    - entering no args when running `check_image.py` should print default values
    - entering args when running `check_image.py` should print entered values
- these three args will need to be retrieved for:
    - folder with images
    - CNN model
    - file containing dognames list
- how to set up and then access argparse arguments

## 8. (Workspace)
- write the function to parse the args and send them back

## 9. Mutable Data Types and Functions
- more about using mutable vs immutable data types in `check_images.py`
- list outside scope of function passed into function can be mutated locally
- list local to function not returned only exists in that function
- list local to function returned by function exists outside it

## 10. Creating Pet Image Labels
- create labels for pet images in `get_pet_labels.py`
- function returns a dictionary with filename keys and list values
    - list contains only the label
- filename labels are the "truth" of the classification
    - used to check how classification went
    - expect 40 kv pairs with lowercase labels, single spacing, correct filenames
- call the function in `main()` check images passing it the `dir` arg
- use `os.listdir` to read files from directory

## 11. (Workspace)
- create checker labels dict from list of pet images

## 12. Classifying Images
- `classify_images` should create classifier labels and compare them to pets
    - store the classifier labels in the results returned by `get_pet_labels`
- `check_images` should be called with parsed args
    - the arg `dir` and the arg `arch`
- return a dictionary of lists mapping filenames to label data
    - list index 0 holds the pet image label
    - list index 1 holds the classifier label
    - list index 2 holds the comparison of labels
- tests should show that:
    - matches between classifiers and pet image labels are real
    - non-matches between classifiers and pet labels are real
    - matches and non-matches together total 40 (of the 40 sample images)

## 13. (Workspace)
- modify `check_images` and especially `classify_images` as outlined

## 14. Classifying Labels as Dogs
- code `adjust_results4_isadog`
- read dog names from text file into a dictionary
- compare dog names to classifier and pet image labels in `results` dict
- update `results` with whether or not labels indicate it's a dog
- `check_images` should run the adjust function passing it the `dogfile` arg

## 15. (Workspace)
- write the adjust method adding label match to indexes 3,4 of each result

## 16. Calculating Results
- build up a dict in `calculates_results_stats` with various percentages
- percentages evaluate matches and correct classifications versus totals

## 17. (Workspace)
- calculate and return results stats

## 18. Printing Results
- code `print_results`
- take results and results stats dicts and print summary
- `results` allows printing of incorrectly classified dogs and breeds

## 19. (Workspace)
- create function to print results
- run batch shell script to test with all three models

## 20. Classify Uploaded Images
- add images to `uploaded_images` folder
- run batch shell script to test with all models
- questions to answer
    - Not all models classified Dog_01 as the same breed. It's a Kuvasz to alexnet, a Golden Retriever to resnet and a Great Pyrenees to vgg. The dog is, in fact, a cream-colored Golden Retriever.
    - Not all models saw Dog_01 as the same breed as mirror-image Dog_02. Vgg switched its bid to Golden Retriever. Resnet leaped to Kuvasz. Alexnet now thinks the flipped dog is a Great Pyrenees.
    - Giraffe and Wheel were reported not-dogs by all but with quite different results. Alexnet guessed a dam and a buckle. Resnet opted for a jaguar/panther and a manhole cover. Vgg saw a llama and a manhole cover.
    - Based on these limited results, vgg looks like the winner, homing in on good choices even when it's off. Resnet is next, at least in the ballpark for all, while alexnet gave some results worth chuckling at, including a total misclassification of a giraffe. The difference in timing was as limited as the dataset, but I'm curious if resnet will be good enough given the extra time required for vgg.

## 21. (Workspace)
- upload the four images to the folder in the workspace

## 22. Final Results
- compare results to the instructors' classification results

## 23. (Workspace)
- 

## 24. Conclusion
- 
