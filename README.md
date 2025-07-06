# capstone_project

# Dynamic Pricing for Urban Parking Lots

## Project Overview

This project implements real-time dynamic pricing models for urban parking lots using streaming data. The goal is to optimize parking lot prices based on occupancy, traffic, queue length, vehicle type, and competitor pricing in nearby lots. The models are designed to adapt prices dynamically to maximize revenue and enhance user experience.

The project includes three pricing models:
- **Model 1:** Baseline Linear Model (price based on occupancy)
- **Model 2:** Demand-Based Model (adds queue, traffic, vehicle type, and special day effects)
- **Model 3:** Competitive Model (adjusts price based on competitor pricing and proximity)

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Tech Stack

- **Python** – Main programming language
- **Pathway** – Real-time streaming data processing
- **Pandas & NumPy** – Data manipulation and numerical calculations
- **Bokeh** – Interactive data visualization
- **Mermaid** – Architecture diagram visualization (embedded in README)
- **Git & GitHub** – Version control and code hosting

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Architecture Diagram

```mermaid
flowchart TD
    CSV_Data["CSV Dataset"]
    Stream_Processor["Pathway Streaming Processor"]
    Pricing_Models["Pricing Models"]
    Model1["Model 1: Baseline"]
    Model2["Model 2: Demand-Based"]
    Model3["Model 3: Competitive"]
    Visualization["Bokeh Visualization"]
    Output["Output JSON / Dashboard"]

    CSV_Data --> Stream_Processor
    Stream_Processor --> Pricing_Models
    Pricing_Models --> Model1
    Pricing_Models --> Model2
    Pricing_Models --> Model3
    Model1 --> Output
    Model2 --> Output
    Model3 --> Output
    Output --> Visualization
