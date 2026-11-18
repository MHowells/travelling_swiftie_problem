# The Travelling *Swiftie* Problem
Can operational research help Taylor Swift plan the perfect tour of London?

In her song *London Boy*, from the album *Lover*, Taylor Swift mentions
several locations in London. However, visiting these locations in the order
that they appear in the song would not necessarily make for efficient journey.

This raises an interesting question: 
**What is the shortest route that visits all these locations?**

Fortunately, operational research provides a way to answer this question
through the *Travelling Salesman Problem* (TSP), a well known problem in
combinatorial optimisation. Doing so, we can help Taylor map out *The Best Day* 
for her and her *London Boy*.

This repository contains the Python code accompanying my article, 
*The Travelling Swiftie Problem*, published in the OR Society's 
*Impact* magazine. It also has a link to the video made for the OR Society's 
OR in Education programme. It also provides the resources referenced in my 
presentations on the topic.

## The Problem

The Travelling Salesman Problem seeks to determine the shortest possible 
route that visits a given set of locations, typically returning to the 
starting point.

For the *Travelling Swiftie Problem*, we consider an *open* variant of the TSP, 
in which the route does not need to return to its starting location.

The problem involves nine locations across London:
- Camden Market
- Highgate
- West End
- Shoreditch
- Hackney
- Bond Street
- Soho
- Hampstead Heath
- Brixton

The objective is to find the shortest route that visits each location exactly 
once, with Brixton as the final destination, so that they can enjoy a night
out as in the song.

## Methodology

Since there are only nine locations, the problem is solved in Python using a 
brute-force approach, which evaluates all possible routes to find the shortest 
one.

The implementation uses:
1. A distance matrix representing the distances between the locations.
2. The `itertools` library to generate all possible permutations of the locations.
3. A dummy destinations to enforce the specified endpoint.
4. A comparison of route distances to determine the optimal solution.

As every feasible route is evaluated, the brute-force approach can establish
an optimal solution for the specified distance matrix. However, the number
of possible routes grows factorially with the number of locations, making this
approach impractical for substantially larger problems.

The implementation is provided in the Jupyter Notebook, 
`travelling_swiftie_problem.ipynb`.

## Results

Using the distance matrix and contraints specified in the notebook, the
minimum total distance is **19.00 miles**.

The optimal route identified is:
Hackney → Shoreditch → Highgate → Hampstead Heath → Camden Market → Soho → Bond Street → West End → Brixton

This is an optimal solution for the distances and assumptions used in the
model. Actual travel distances and the most practical route may differ
depending on the mode of transport, traffic conditions, and other 
real-world factors.

## Running the Code

The project is implemented in Python and provided as a Jupyter Notebook. 

To run the code locally:

***1. Clone the repository:***
```bash
git clone https://github.com/MHowells/travelling_swiftie_problem.git
``` 

***2. Install the required dependencies:***
```bash
pip install -r requirements.txt
pip install jupyter
```

***3. Open the Jupyter Notebook:***
```bash
jupyter notebook travelling_swiftie_problem.ipynb
```

## Publication and Outreach

This project was developed as an accessible introduction to combinatorial 
optimisation, demonstrating how operational research can be applied to an 
entertaining problem inspired by popular culture.

- **Article**: [The Travelling Swiftie Problem](https://www.tandfonline.com/doi/full/10.1080/2058802X.2024.2388417) published in the OR Society's *Impact* magazine.
- **Short Video**: [The Travelling Swiftie Problem](https://youtu.be/6qrr64Ba9ug?si=LbR9Cau8lNaxbj-K) produced for the OR Society's OR in Education programme.
- **Conference Presentation**: *The Travelling Swiftie Problem: Solving the Routing Problem of a London Boy* presented at the [OR Society's Systems Conference (2024)](https://www.theorsociety.com/ORS/ORS/Event_Display.aspx?EventKey=STCONF24).

## Resources

The following resources are referenced in the article and accompanying talk.

### The Travelling Swiftie Problem
- [*London Boy* by Taylor Swift](https://www.youtube.com/watch?v=VsKoOH6DVys&ab_channel=TaylorSwiftVEVO)
- [The Twitter post that inspired it all](https://x.com/_EthanBeer/status/1164960418688831489)
- [OpenStreetMap](https://www.openstreetmap.org/)

### Routing Optimisation
- [Google OR-Tools - Routing](https://developers.google.com/optimization/routing)
- [Prof. Güneş Erdoğan's VRP Spreadsheet Solver](https://people.bath.ac.uk/ge277/vrp-spreadsheet-solver/)
- [Prof. Rhyd Lewis' Resources](https://rhydlewis.eu/#resources)

### Further Reading
- Sciortino, M., Lewis, R. & Thompson, J. A School Bus Routing Heuristic Algorithm Allowing Heterogeneous Fleets and Bus Stop Selection. SN COMPUT. SCI. 4, 74 (2023). [https://doi.org/10.1007/s42979-022-01466-6](https://doi.org/10.1007/s42979-022-01466-6) 
- Gartner, D., Frey, M., & Kolisch, R. (2018). Hospital-wide therapist scheduling and routing: Exact and heuristic methods. IISE Transactions on Healthcare Systems Engineering, 8(4), 268–279. [https://doi.org/10.1080/24725579.2018.1530314](https://doi.org/10.1080/24725579.2018.1530314)

## Contact
If you have any questions about the project, or would like to keep up with 
my work, you can find me here:

- **Email**: [HowellsMA@cardiff.ac.uk](mailto:HowellsMA@cardiff.ac.uk)
- **LinkedIn**: [Matthew Howells](https://www.linkedin.com/in/matthewahowells/)
- **Bluesky**: [@HowellsMA.bsky.social](https://bsky.app/profile/howellsma.bsky.social)
- **Google Scholar**: [Matthew Howells](https://scholar.google.com/citations?user=71sfmvwAAAAJ&hl=en)



