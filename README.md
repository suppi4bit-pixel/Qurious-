# Qurious

**An AI-based quantum algorithm learning platform**
*From curious to quantum-ready.*

> ## 🚧 Work in progress
> This is an **early prototype** built for **Smart India Hackathon 2026, problem statement SIH26140**
> (AI-Based Interactive Quantum Algorithm Learning Platform, Egreen Quanta).
> It demonstrates the **core learning loop only**. Several features are planned but **not built yet**;
> see the status table below. Expect rough edges.

## The idea
Learn → Build → Simulate → Visualize → Understand, in one place.
Students build a quantum circuit, run it on a real simulator, see the resulting state on Bloch spheres
and probability bars, and get an explanation of *that specific result*.

## Status

| Area | Status |
|---|---|
| Circuit builder (X, Y, Z, H, S, T, CNOT, 3 qubits) | Working |
| Simulation on Qiskit Aer (FastAPI backend) | Working |
| Local in-browser simulator (fallback) | Working |
| Bloch spheres and measurement probabilities | Working |
| Lesson 1 (Bell state) with topic quiz and concept trail | Working (one lesson) |
| AI tutor grounded in the simulated result | Working, early; needs an API key on the server |
| Additional lessons (Deutsch-Jozsa, Grover, QAOA, VQE) | Planned |
| More qubits and a code editor | Planned |
| PennyLane, Cirq and qBraid backends | Planned |
| User accounts, saved progress, analytics | Planned |
| Instructor dashboard, auto-graded coding challenges | Planned |

## Verification
`pytest` checks Qiskit Aer results against known states (Bell, GHZ, Bloch axes) and against an
independent NumPy simulator on 150 random circuits.

## Run locally
    pip install -r requirements.txt
    uvicorn main:app --port 8000        # open http://localhost:8000
Set `ANTHROPIC_API_KEY` to enable the AI tutor. Tests: `pip install -r requirements-dev.txt && pytest -v`

## Tech
Python, FastAPI, Qiskit Aer, vanilla JavaScript front end, Claude API for the tutor.

## Team
Team Name: Six Degrees
