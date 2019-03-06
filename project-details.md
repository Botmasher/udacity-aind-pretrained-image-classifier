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
- 

## 15. (Workspace)
- 

## 16. Calculating Results
- 

## 17. (Workspace)
- 

## 18. Printing Results
- 

## 19. (Workspace)
- 

## 20. Classify Uploaded Images
- 

## 21. (Workspace)
- 

## 22. Final Results
- 

## 23. (Workspace)
- 

## 24. Conclusion
- 
