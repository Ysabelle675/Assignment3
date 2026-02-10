# Assignment3
Video link: https://www.canva.com/design/DAHAZJfIzPE/fCjx0D5XhW6wb6VwQaPF3A/edit?utm_content=DAHAZJfIzPE&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton
main.cpp link: https://replit.com/@ysanchez76/Assignment3#main.cpp
Transcript: https://share.google/aimode/woCxQsk6nWiNaHkyY
Assignment 3 code in case the main.cpp upload link does not work:

#include <iomanip> // For std::fixed and std::setprecision
#include <iostream>

int main() {
  const int SIZE = 30;
  int scores[SIZE] = {78, 92, 65, 88, 45, 100, 72, 81, 59, 96,
                      84, 67, 91, 53, 77, 89,  62, 98, 74, 85,
                      48, 93, 70, 82, 66, 95,  55, 87, 79, 64};

  int sum = 0;
  int highest = scores[0];
  int lowest = scores[0];
  int passedCount = 0;
  int aCount = 0;

  for (int i = 0; i < SIZE; i++) {
    sum += scores[i];

    if (scores[i] > highest)
      highest = scores[i];
    if (scores[i] < lowest)
      lowest = scores[i];
    if (scores[i] >= 60)
      passedCount++;
    if (scores[i] >= 90)
      aCount++;
  }

  double average = static_cast<double>(sum) / SIZE;

  std::cout << "Number of students: " << SIZE << std::endl;
  std::cout << std::fixed << std::setprecision(2);
  std::cout << "Average score:      " << average << std::endl;
  std::cout << "Highest score:      " << highest << std::endl;
  std::cout << "Lowest score:       " << lowest << std::endl;
  std::cout << "Students passed:    " << passedCount << "  (>= 60)"
            << std::endl;
  std::cout << "Students with A:    " << aCount << "   (>= 90)" << std::endl;

  std::cout << "\nScores in original order:" << std::endl;
  for (int s : scores) {
    std::cout << s << " ";
  }
  std::cout << std::endl;

  std::cout << "Scores in reverse order:" << std::endl;
  for (int i = SIZE - 1; i >= 0; i--) {
    std::cout << scores[i] << " ";
  }
  std::cout << std::endl;

  return 0;
}
