# Αποθετήριο του μαθήματος: Ανάλυση Δεδομένων

## Ονοματεπώνυμο
## [Προφίλ Github: aggelos2000430](https://github.com/aggelos2000430)

| Εβδομάδα | Παραδοτέα | Ολοκλήρωση Παραδοτέου :heavy_check_mark: |
| --- | --- | --- |
| 1 | Δημιουργία προφίλ στην πλατφόρμα + Fork του αποθετηρίου του μαθήματος|  |
| 2 | Δημιουργία του αρχείου .md στο προφίλ σας και αντιγραφή του πίνακα παραδοτέων στο προσωπικό σας αρχείο με τίτλο το ονοματεπώνυμο σας με λατινικούς χαρακτήρες που αποτελεί και την τελική αναφορά του μαθήματος|  |
| 3 | Συγγραφή μιας σύντωμης περιγραφής για την σημασία της ανάλυσης δεδομένων στον σύγχρονο κόσμο |  |
| 4 | Εκτέλεση του κώδικα στο σύστημά σας |  |
| 5 | Αντιγραφή του python κώδικα και λεπτομερής σχολιασμός του, εντός της αναφοράς σας |  |
| 6 | Προφορική υποστήριξη της αναφοράς σας |  |

Data analysis is a process of inspecting, cleansing, transforming, and modeling data with the goal of discovering useful information, informing conclusions, and supporting decision-making.[1] Data analysis has multiple facets and approaches, encompassing diverse techniques under a variety of names, and is used in different business, science, and social science domains.[2] In today's business world, data analysis plays a role in making decisions more scientific and helping businesses operate more effectively.[3]

Data mining is a particular data analysis technique that focuses on statistical modeling and knowledge discovery for predictive rather than purely descriptive purposes, while business intelligence covers data analysis that relies heavily on aggregation, focusing mainly on business information.[4] In statistical applications, data analysis can be divided into descriptive statistics, exploratory data analysis (EDA), and confirmatory data analysis (CDA).[5] EDA focuses on discovering new features in the data while CDA focuses on confirming or falsifying existing hypotheses.[6][7] Predictive analytics focuses on the application of statistical models for predictive forecasting or classification, while text analytics applies statistical, linguistic, and structural techniques to extract and classify information from textual sources, a species of unstructured data. All of the above are varieties of data analysis.[8]

Data integration is a precursor to data analysis, and data analysis is closely linked to data visualization and data dissemination.[9]

with open('sorting_runtimes.txt', 'r') as file:
    data = file.read().splitlines()

runtimes = {}

for i in range(0, len(data), 8):
    algorithm = data[i].split(' - ')[0]
    runtime = float(data[i+1].split(' - ')[1].split(' ')[0])
    runtimes[algorithm] = runtimes.get(algorithm, 0) + runtime

for algorithm, runtime in runtimes.items():
    avg_runtime = runtime / 10

fastest_algorithm = min(runtimes.items(), key=lambda x: x[1])
print(f"The fastest sorting algorithm is {fastest_algorithm[0]} with an average runtime of {fastest_algorithm[1]/10:.6f} seconds.")
