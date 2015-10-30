# Setup

It's written in Ruby.  You'll need ruby.
You'll need bundler (`gem install bundler`).
Then `bundle install` from the repo dir, to get all the libraries.

Copy scrape_course_data.rb.tmpl to scrape_course_data.rb 

# Usage

There are several things you'll need to change at the bottom of scrape_course_data.rb.
Put your USERID and your PIN for oscar.gatech.edu.  This is how it gets the course data.
Put in the TERM you want, right now this is Spring 2016.
Change your interests and what you've taken to get the best output.

# Example output

NUMBER | ALT  | TITLE                          | WEIGHT | CAPACITY | REMAINING | IS_FOUNDATIONAL_TO_S | SPECIALIZATIONS_TO_S         | IS_INTERESTING_TO_S
-------|------|--------------------------------|--------|----------|-----------|----------------------|------------------------------|--------------------
6250   |      | Computer Networks              | 40     | 200      | 197       | Yes                  | Systems                      | Yes
7637   |      | Knowledge-Based AI             | 40     | 250      | 247       | Yes                  | IA Intell                    | Yes
7641   |      | Machine Learning               | 40     | 200      | 193       | Yes                  | Robotics, IA Intell, ML      | Yes
6210   |      | Adv Operating Systems          | 25     | 200      | 200       | Yes                  | Systems                      | No
6290   |      | High Perform Comput Arch       | 25     | 200      | 200       | Yes                  | Systems, HPC                 | No
6300   |      | Software Dev Process           | 25     | 200      | 193       | Yes                  | Systems, IA Intell           | No
6310   |      | Software Arch & Design         | 25     | 200      | 198       | Yes                  | Systems                      | No
6400   |      | DB Sys Concepts& Design        | 25     | 200      | 193       | Yes                  | Systems                      | No
6440   |      | Intro Health Informatics       | 25     | 200      | 195       | No                   | IA Intell                    | Yes
6460   |      | Educ Tech-Foundations          | 25     | 100      | 96        | No                   | IA Intell                    | Yes
6475   |      | Comp. Photography              | 25     | 200      | 200       | No                   | Robotics                     | Yes
6505   |      | Computability&Algorithms       | 25     | 200      | 195       | Yes                  | Robotics, IA Intell, ML      | No
7646   |      | Mach Learn For Trading         | 25     | 250      | 246       | No                   | ML                           | Yes
6035   |      | Intro To Info Security         | 10     | 200      | 197       | No                   | Systems                      | No
6340   |      | Software Analysis & Test       | 10     | 200      | 199       | No                   | Systems                      | No
6476   | 7495 | Computer Vision                | 10     | 200      | 198       | Yes                  | Robotics                     | Yes
8803   |      | Special TopicsAI in Robotic... | 10     | 200      | 200       | No                   | Robotics, HPC, IA Intell, ML | No
8803   |      | Special TopicsIntro to Oper... | 10     | 200      | 199       | No                   | Robotics, HPC, IA Intell, ML | No
8803   |      | Special TopicsReinforcement... | 10     | 200      | 196       | No                   | Robotics, HPC, IA Intell, ML | No
8803   |      | Special TopicsEmbedded Soft... | 10     | 200      | 198       | No                   | Robotics, HPC, IA Intell, ML | No         


# Notes

Right now it is just running with the Online data set for GT's OMSCS.
It references foundational classes, specializations, your interests and availability for the given TERM to derive a weight (score).  The higher the score, the better the option is.

Also, it will likely only work in Linux (64 bit) right off the bat.
It uses poltergeist (phantomjs) to process all the javascript.
Just replace the contents of the bin dir with the phantomjs for your system.
