### Data Parallelism vs Task Parallelism
Data: 300 exams dibagi 3 menjadi 100 exams
Task: 300 exams, tiap exams ada 15 questions, dibagi 3 menjadi 1-5,6-10,11-15.

### Coordination
- Communication, one or more core send their partial sum to other cores
- Load balancing, balances load/work evenly so no one core is overworked
- Synchronization

## Types of Parallel Systems
- Shared-memory
- Distributed-memory, menggunakan network (message passing)

## Flynn's Taxonomy
Single/multiple instruction stream, single/multiple data stream
- SISD
- SIMD, **data parallelism**, (ex. GPU)
	Efficient for large data parallel problems, but not for more complex problems, as some ALU can be under utilized
	
- MISD
- MIMD
