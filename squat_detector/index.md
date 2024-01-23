# Stay Fit & Get Your Caffeine Fix with AI-Powered Squat Detection


## Introduction

What if your workout routine could be seamlessly integrated with a reward system that acknowledges your efforts with something as delightful as a cup of coffee? We've developed a unique approach to fitness with a technological spin: using face-recognition from the AIY Vision Kit to detect squats and reward you with a free coffee after your exercise.

### The Concept

This idea leverages a face-detection model to monitor a person's face within a video feed. When the system detects that the face has moved below a certain height threshold, it counts as a squat. Keep up the good work, and once you hit the set number of squats, a signal prompts a coffee machine to brew a fresh cup.

### Requirements

To utilize this innovative system, ensure you have the following:

#### Hardware
- AIY Vision Kit

#### Software
- Python3

### Execution

Run the `main_loop.py` script, which will engage the Vision AI Camera's face-detection feature to identify faces in the video. Achieve five squats, and the system triggers an event via a GPIO pin.

### Customization for Various Rewards

The flexibility of this system is one of its greatest perks. Although we chose a coffee machine as the reward mechanism, you can tailor it to trigger any event or device of your choice. It's all about making your workout rewarding and enjoyable.

Embrace the blend of technology and fitness, and add a fun, rewarding twist to your exercise routine. Stay fit, stay healthy, and let technology make it a little more rewarding!


