# MDTMultiAgent

MDT_Pathway_Generation/
│
├── Input
│   ├── DiagnosedPatientInput
│   │   ├── DiagnosisReport
│   │   ├── Comorbidities
│   │   ├── SeverityLevel
│   │   ├── ClinicalPriority
│   │   └── OptionalClinicalEvidence
│   │       ├── ChiefComplaint
│   │       ├── Demographics
│   │       ├── MedicalHistory
│   │       └── TestResults
│   │
│   └── ResourceStateInput
│       ├── BedAvailability
│       ├── ICUCapacity
│       ├── TheatreSlots
│       ├── StaffAvailability
│       ├── DiagnosticCapacity
│       └── WaitingTime
│
├── Step_1_Identify_Involved_Services
│   ├── SpecialtyDepartment
│   │   ├── Cardiology
│   │   ├── Respiratory
│   │   ├── Neurology
│   │   ├── Gastroenterology
│   │   ├── Nephrology
│   │   ├── Oncology
│   │   ├── Orthopaedics
│   │   ├── GeneralSurgery
│   │   └── InfectiousDisease
│   │
│   ├── Diagnostics
│   │   ├── Laboratory
│   │   ├── Radiology
│   │   ├── Pathology
│   │   └── Microbiology
│   │
│   ├── Surgery_Theatre
│   │   ├── GeneralSurgeryTheatre
│   │   ├── OrthopaedicTheatre
│   │   ├── CardiacTheatre
│   │   └── EmergencyTheatre
│   │
│   ├── Ward_or_ICU
│   │   ├── GeneralWard
│   │   ├── SpecialtyWard
│   │   ├── HDU
│   │   └── ICU
│   │
│   ├── Nursing
│   │   ├── WardNursing
│   │   ├── SpecialistNursing
│   │   └── CriticalCareNursing
│   │
│   ├── Rehabilitation
│   │   ├── Physiotherapy
│   │   ├── OccupationalTherapy
│   │   ├── SpeechAndLanguageTherapy
│   │   └── Dietetics
│   │
│   ├── Pharmacy
│   │   ├── MedicationReview
│   │   ├── AntibioticSupport
│   │   └── HighRiskDrugManagement
│   │
│   └── DischargePlanning
│       ├── SocialCarePlanning
│       ├── CommunityFollowUp
│       ├── HomeCareSupport
│       └── PalliativePlanning
│
├── Step_2_Call_Relevant_Agents
│   ├── Core_Coordination
│   │   ├── OrchestratorAgent
│   │   ├── MDTCoordinatorAgent
│   │   ├── PatientSummaryAgent
│   │   └── TimelineGeneratorAgent
│   │
│   ├── SpecialtyDepartment_Agents
│   │   ├── Cardiology
│   │   │   ├── CardiologistAgent
│   │   │   └── CardiologyRegistrarAgent
│   │   ├── Respiratory
│   │   │   ├── RespiratoryConsultantAgent
│   │   │   └── RespiratoryRegistrarAgent
│   │   ├── Neurology
│   │   │   └── NeurologistAgent
│   │   ├── Gastroenterology
│   │   │   └── GastroenterologistAgent
│   │   ├── Nephrology
│   │   │   └── NephrologistAgent
│   │   ├── Oncology
│   │   │   └── OncologistAgent
│   │   ├── Orthopaedics
│   │   │   └── OrthopaedicSurgeonAgent
│   │   ├── GeneralSurgery
│   │   │   └── GeneralSurgeonAgent
│   │   └── InfectiousDisease
│   │       └── InfectiousDiseaseAgent
│   │
│   ├── Diagnostics_Agents
│   │   ├── Laboratory
│   │   │   └── LaboratoryAgent
│   │   ├── Radiology
│   │   │   └── RadiologyAgent
│   │   ├── Pathology
│   │   │   └── PathologyAgent
│   │   └── Microbiology
│   │       └── MicrobiologyAgent
│   │
│   ├── Surgery_Theatre_Agents
│   │   ├── SurgeonAgent
│   │   ├── AnaesthetistAgent
│   │   ├── TheatreCoordinatorAgent
│   │   └── PerioperativeCareAgent
│   │
│   ├── Ward_or_ICU_Agents
│   │   ├── WardDoctorAgent
│   │   ├── ICUDoctorAgent
│   │   ├── BedManagerAgent
│   │   └── CriticalCareAgent
│   │
│   ├── Nursing_Agents
│   │   ├── NursingAgent
│   │   ├── SpecialistNurseAgent
│   │   └── CriticalCareNurseAgent
│   │
│   ├── Rehabilitation_Agents
│   │   ├── PhysiotherapyAgent
│   │   ├── OccupationalTherapyAgent
│   │   ├── SpeechTherapyAgent
│   │   └── DietitianAgent
│   │
│   ├── Pharmacy_Agents
│   │   ├── PharmacistAgent
│   │   └── AntibioticStewardshipAgent
│   │
│   ├── DischargePlanning_Agents
│   │   ├── DischargePlanningAgent
│   │   ├── SocialCareAgent
│   │   ├── CommunityCareAgent
│   │   └── PalliativeCareAgent
│   │
│   └── Cross_Cutting_Agents
│       ├── ResourceManagerAgent
│       ├── PatientVoiceAgent
│       └── SafetyCriticAgent
│
├── Step_3_MDT_Discussion_Loop
│   ├── AssignSpeakingWeight
│   │   ├── by_DiseaseSeverity
│   │   ├── by_ClinicalPriority
│   │   ├── by_SpecialtyRelevance
│   │   └── by_ResourceConstraint
│   │
│   ├── CollectOpinions
│   ├── IntegrateDraftPlan
│   ├── SafetyReview
│   ├── ConflictCheck
│   ├── FeasibilityCheck
│   └── ReviseUntilStable
│
├── Step_4_Generate_Final_Output
│   ├── TreatmentPlan
│   ├── CarePlan
│   ├── ResourceManagementPlan
│   └── TimeSpecificPathwaySchedule
│       ├── TestTimeline
│       ├── TreatmentTimeline
│       ├── Bed_or_ICU_Arrangement
│       ├── TransferPlan
│       ├── RehabilitationPlan
│       └── DischargePlan
│
└── Final_Output
    └── PatientPathwayTimeline
