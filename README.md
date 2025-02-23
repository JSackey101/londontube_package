
London Underground Journey Planner Package
==========================================

This Python package provides tools for planning journeys on the London Underground network. It is designed to 
utilize real-time data to calculate the most efficient routes between stations, considering current network 
conditions and disruptions.

Components
----------
1. journey_planner.py: 
   - Contains the main functionality to plan journeys. 
   - It takes a start and destination station, along with a date, and returns the optimal journey path and duration.

2. Network.py:
   - Defines the Network class, used to represent the network of the London Underground.
   - It includes functionality to manipulate and query network data, such as merging networks and retrieving network attributes.

3. query.py:
   - Handles communication with external web services to fetch real-time data about the London Underground network.
   - Provides functions to query specific aspects of the network, like line connections, and integrates this data into the Network class.

Usage
-----
The package can be used to plan journeys across the London Underground. It can handle queries for specific dates 
and times, taking into account real-time network conditions and disruptions. This makes it an invaluable tool for 
both daily commuters and tourists seeking to navigate the city efficiently.

Developed as part of the UCL-COMP0233 course, this package demonstrates the application of network analysis, 
data fetching from web services, and object-oriented programming in Python to solve real-world problems.

Example
-------
To plan a journey from 'Waterloo' to 'Warren Street' on 2023-12-19, and save the plot as a png file::

    $journey-planner --plot "waterloo" "warren street" 2023-12-19
    Date: 2023-12-19
    Journey will take 9 minutes.
    Start: Waterloo
    Westminster
    Green Park
    Oxford Circus
    End: Warren Street
    Plot saved to journey_from_Waterloo_to_Warren_Street.png

This package is a prototype and is intended for educational purposes in network analysis and Python programming.

User Guide
==========

Installation
------------
To install the londontube package, follow these steps:

1. Ensure you have Python installed on your system. Python version should be >=3.7 and <3.11.
2. Navigate to the directory containing the package files in your terminal or command prompt.
3. Run the installation command::

    pip install .

   This will install the package along with its dependencies.

Example Workflow
----------------
After installation, you can use the package to plan journeys on the London tube network. Here's a step-by-step example:

1. Import the `journey-planner` function from the `journey_planner` module::

    from journey_planner import journey_planner

2. Define your start and destination stations along with the date of the journey and the status for plot. For example, to plan a journey from 'Waterloo' to 'Baker Street' on January 1, 2023, and finally plot it::

    plot = True
    start = "Waterloo"
    dest = "Warren Street"
    setoff_date = "2023-12-19"

3. Call the `journey_planner` function with these parameters::

    journey_planner(plot, start, dest, setoff_date)

4. The function will return the journey route and duration::

    Date: 2023-12-19
    Journey will take 9 minutes.
    Start: Waterloo
    Westminster
    Green Park
    Oxford Circus
    End: Warren Street
    Plot saved to journey_from_Waterloo_to_Warren_Street.png
    

This will output the sequence of stations on the journey path and the total journey duration in minutes.


Developer Guide
===============

Contributing to the Repository
------------------------------
We welcome contributions from the community. To contribute to this project, please follow these steps:

1. Fork the Repository:
   - Navigate to the GitHub page of the repository and use the 'Fork' button to create your own copy.

2. Clone the Forked Repository:
   - Clone your forked repository to your local machine::
    
        git clone https://github.com/your-username/london-journey-planner.git

3. Create a New Branch:
   - Navigate into the cloned directory and create a new branch for your feature or bug fix::
    
        git checkout -b your-feature-branch

4. Make Your Changes:
   - Implement your feature or bug fix.

5. Write Tests:
   - Add or update tests to cover your changes.

6. Follow the Coding Style:
   - Ensure your code adheres to the project's coding standards (PEP 8 for Python).

7. Commit Your Changes:
   - Commit your changes with a clear and descriptive commit message.

8. Push to GitHub:
   - Push your changes to your fork on GitHub.

9. Submit a Pull Request:
   - Open a pull request from your feature branch to the main repository.

Your pull request will be reviewed by the maintainers and merged into the main codebase after review and approval.

Testing the Code
----------------
To ensure the reliability of the package, please follow these guidelines for testing:

1. Write Unit Tests:
   - Add unit tests for every new feature or bug fix in the `tests` directory.
   - Use Python's built-in `unittest` framework or a framework like `pytest`.

2. Run Tests Locally:
   - Run the test suite locally to ensure that all tests pass before submitting a pull request.
   - You can use commands like `python -m unittest discover` or `pytest`.

3. Continuous Integration:
   - The project uses continuous integration (CI) tools (e.g., GitHub Actions, Travis CI). Ensure that your code passes all CI checks.

Coding Style
------------
This project adheres to the PEP 8 style guide for Python code. Please ensure your code follows these guidelines:

- Use 4 spaces for indentation.
- Limit lines to 79 characters.
- Use descriptive variable and function names.
- Document your code with docstrings.

Additional Resources
--------------------
For more information on contributing, testing, and coding styles, please refer to the following resources:

- PEP 8 Style Guide: https://www.python.org/dev/peps/pep-0008/
- Git and GitHub Guide: https://guides.github.com/
- Python Testing: https://docs.python.org/3/library/unittest.html

We appreciate your interest in contributing to the London Underground Journey Planner package and look forward to your valuable contributions!



Functions in the Package
========================
1. Network.py
-------------

```londontube.Network.Network.__add__```

```londontube.Network.Network.distant_neighbours```

```londontube.Network.Network.dijkstra```

2. query.py
-----------

```londontube.query.query_line_connections```

```londontube.query.query_station_information```

```londontube.query.query_station_num```

```londontube.query.parse_station_data```

```londontube.query.query_disruptions```

```londontube.query.parse_disruptions_data```

```londontube.query.real_time_network```

3. journey_planner.py
---------------------

```londontube.journey_planner.plan_journey```

```londontube.journey_planner.plot_journey```

```londontube.journey_planner.journey_planner```
