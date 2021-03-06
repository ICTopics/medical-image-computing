---
cover: "lungcancer.jpg"
title: "Detection of Lung Cancer"
description: "In this section, you'll learn about how in the recent past, doctors and computer scientists have come together to develop better diagnosis technology, using AI, in order to fight lung cancer."
sources:
- name: "Medical Futurist"
  url: "http://medicalfuturist.com/the-future-of-radiology-and-ai/"
- name: "Data Science Bowl"
  url: "https://datasciencebowl.com/competitions/turning-machine-intelligence-against-lung-cancer/"
- name: "Cancer Research UK"
  url: "http://www.cancerresearchuk.org/health-professional/cancer-statistics/statistics-by-cancer-type/lung-cancer"
- name: "ZD Net"
  url: "http://www.zdnet.com/article/google-takes-health-care-to-the-cloud-with-new-api-partnerships/"
- name: "Google Blog"
  url: "https://blog.google/topics/google-cloud/google-cloud-healthcare-new-apis-customers-partners-and-security-updates/"
- name: "Medium"
  url: "https://tinyurl.com/yabp56q4"
- name: "Project LUNA"
  url: "https://luna16.grand-challenge.org/results/"
- name: "Pulmonary Nodule Detection in CT Images: False Positive Reduction Using Multi-View Convolutional Networks"
  url: "http://ieeexplore.ieee.org/abstract/document/7422783/"
- name: "Project AiAi"
  url: "https://aiai.care/"
- name: "Genetic Deep Learning for Lung Cancer Screening"
  url: "https://www.dropbox.com/s/0xw2r5t5ge0sjam/Genetic%20Deep%20Learning%20for%20Lung%20Cancer%20Screening.pdf?dl=0"
imgs:
- name: "Data Science Bowl"
  figure: 1
  url: "https://3zh2ja3name32zs0my28kd3c-wpengine.netdna-ssl.com/wp-content/uploads/2017/11/lung-illustration-web-3.5.png"
- name: "How to interpret CT scans of your lung"
  figure: 2
  url: "http://www.website-go.com/acc/"
- name: "Everyday Health"
  url: "https://www.everydayhealth.com/lung-cancer/easing-pain-of-lung-cancer.aspx"
---

## How does AI relate to Lung Cancer? {#top}

Lung cancer is an area in which artificial intelligence is starting to become more prominent. It is the third most common type of cancer in the UK, and accounts for 13% of all diagnoses. 130 people a day are diagnosed with lung cancer. The survival rates for over 10 years are only 5%, however 89% of cases are preventable. This is why people are suggesting that machine learning could be used to diagnose these cases more effectively, give treatment earlier, and increase survival rates.

Earlier detection is important because it allows lots of treatment options which would not be available if the cancer is found at a later stage. CT scans, which are the most common method of detection currently, can give false-positive readings and this is why doctors and computer scientists think that machine learning can be used to increase the accuracy and reliability of scan reading.

![Some facts on lung cancer](content-images/lung1.png){ width=100% #fig:1}

## How would it work?

Lung cancer can start off as a small nodule which occurs in an asymptomatic patient - a patient infected but not presenting any symptoms. Screening imaging is the process of looking for these, and diagnosing them before they get worse. When a patient starts getting symptoms, and we detect these small nodules which aren't the cause of the symptoms, these are called incidentally detected nodules. Nodules are classed as being between 1 and 3cm in diameter, and a mass is over 3cm in diameter. Anything below 1cm in diameter is a micronodule.

CT scans are currently the best way to look for these, and PET-CT scans are the best way to look at the behaviour of them, which allows doctors to predict the risk of cancer they impose. Nodules can come in many different shapes, and lots of different features, such as size, location and growth, help radiologists predict if it is cancerous.

Radiologists who are looking for nodules are prone to missing them, as they can be very well hidden, and so this is where machine learning can come into play - to help make the detection of nodules more accurate. The software currently used, called Computer Assisted Detection (CAD), is highly sensitive, but not very specific, so gives a lot of false positives, and so isn't accurate enough to be used in practice.

This is why machine learning is now being considered; in order to improve specificity. The LUNA (LUng Nodule Analysis) Challenge from in 2016, which focused on reducing the number of false positives given by ordinary CAD software. The other big challenge was the Data Science Bowl. Both of these are described in detail below.

## Lung Nodule Analysis (LUNA) Challenge 2016

This competition had 2 main challenges: Nodule Detection (NDET) and False Positive Reduction (NPRED). These use raw CT scans to detect locations of possible nodules, and give these locations probabilities of being a nodule. The task essentially says whether each location is or is not a nodule.

The competitors were given a set of data containing 888 CT scans, which needed to be split into testing and training data. The algorithm they develop has to be done on the training data, and then results are calculated by running the algorithm on the testing data, and seeing the accuracy of the results. The testing data is split into 10 subsets, so that there can be cross-validation to make sure that the algorithm is consistent.

Amongst the submissions was a multi-stream CNN used to integrate 3D in the classification of pulmonary nodules. This architecture aimed to classify points of interest in chest CT scans as nodules or not. For each candidate nodule fed into the network, a set of 2D patches with different orientation planes is considered. Multiple streams of 2D convolution networks then process these sets. A dedicated fusion method finally merges their outputs to give the final classification. The network performed with a high detection sensitivity above 85%, and was particularly effective in reducing "false positives", results wrongly indicating the presence of a nodule. 

![Lung nodule CT scan](content-images/lungNodule.jpg){#fig:2}

## Data Science Bowl 2017

This was a competition aimed at detecting lung cancer using machine learning. The competitors were given 1000 anonymous pictures of lung scans, and had to use these to find patters in data which could later lead to detection and diagnosis, to improve lung cancer screening technology.

The algorithms could detect which legions in the lungs are cancerous, which is an improvement on current methods like CT scans, which often give false-positive readings.

There were over 18,000 algorithms developed during the challenge, with the goal of giving them to actual radiologists, so that they can be used in real time in order to diagnose patients.

## Project AiAi

This is an open source project for lung cancer screening using x-rays. While these may not be as accurate as CT scans, thus making detection harder, x-ray machines are much more common in hospitals, especially in developing countries, and therefore this technology would be much more widely available than the equivalent with CT scanners.

Their aim is to reduce screening time and cost by 90%, and increase survival probability by 5x. The project used machine learning on over 250,000 chest x-rays to build a CAD tool.

## Genetic Deep Learning

A startup called Innovation DX is using genetic deep learning for lung cancer screening. Genetic deep learning is an evolution of convolutional neural networks. They *"injected convolution and pooling layers with pseudorandom hyperparameters into a minimal architecture and then optimized the weights through back propagation on the training set"*. A pseudorandom hyperparameter is a parameter for which the value is set before the learning takes place, and satisfies at least one statistical test for randomness, even though it is produced by a definite mathematical procedure. They inserted these into a basic neural network, and then used back propagation, explained in detail on the [Introduction to Neural Networks](/introduction-neural-nets.html) page, to optimise the neural network with the training data.

Optimisations like this to convolutional neural networks allow them to be specially adapted to medical problems, and make them more efficient in detection and diagnosis. This is why lots of competitions, such as the two above, are trying to entice computer scientists to develop these.

## Problems... and potential solutions?

Lots of doctors are wary of how to store lots of data for machine learning programs to work properly, due to patient confidentiality laws. However, the FDA did approve a cloud-based deep learning algorithm for cardiac imaging in 2017, which shows that in the future, it will be more common placed in patient diagnosis.

In March 2018, Google introduced a new Cloud Healthcare API, which aims to create a secure service which can be used to implement Artificial Intelligence and Machine Learning on lots of healthcare data. Working with the Stanford School of Medicine and other partners, their aim is to "help transform the healthcare industry through the use of cloud technologies and machine learning".
