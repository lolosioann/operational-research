# Operations Research Project 2025

## Overview

This repository contains the solution to the 2025 course project for the *Operations Research* course at the School of Electrical and Computer Engineering, Aristotle University of Thessaloniki.

It addresses two classical optimization problems:

1. **Timetabling Problem**  
   Generation of a feasible weekly class schedule for two school sections, taking into account teacher availability, subject durations, and pedagogical constraints.

2. **Facility Location Problem**  
   Determination of the optimal subset of warehouse locations to open and the corresponding allocation of shipments to minimize total fixed and transportation costs while satisfying customer demands.


## Problem 1: Timetabling

### Problem Description
- Two school sections
- Shared teachers, except for Math and PE
- Time slots: 4 per day, Monday–Friday
- All classes last 2 hours
- Constraints include:
  - Teacher absences
  - Reserved time slots
  - Only one subject per day per section
  - PE must occur in a fixed slot

### Features
- Uses Python enums and dictionaries to model teachers, subjects, and constraints
- MILP formulation solved using **Gurobi**
- Generates a readable timetable using `pandas` tables


## Problem 2: Facility Location

### Problem Description
- 12 potential warehouse locations
- 12 customer sites with known demands
- Transportation costs vary and may be infeasible (∞)
- Each warehouse has a capacity and fixed installation cost

### Features
- MILP model with:
  - Binary variables for warehouse opening
  - Continuous variables for shipment volumes
- Solved using **Gurobi**
- Excludes infeasible delivery routes
- Produces:
  - Total cost summary
  - List of open warehouses
  - Shipment allocation details

## Requirements

- Python
- Gurobi 
- pandas
- numpy
- matplotlib
- gurobipy

**Ensure you have a valid Gurobi license for academic use.**
