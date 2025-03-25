# User Adoption Analysis Summary

## Objective  
Identify which factors predict future user adoption, defined as logging into the product on **three separate days within any rolling seven-day period**.

## Approach

1. **Adoption Labeling**  
   Users were labeled as *adopted* if they logged in on 3 separate days within any 7-day window using login records from `takehome_user_engagement.csv`.

2. **Feature Engineering**  
   Features were extracted from `takehome_users.csv`, including:
   - Signup method (`creation_source`)
   - Referral status (`invited_by_user_id`)
   - Marketing email opt-in flags
   - Temporal features (excluded from insight analysis)

3. **Analysis**  
   Adoption rates were compared across user groups, with focus on actionable business factors rather than time-based predictors.

## Key Findings

| Feature                  | Insight                                                                 |
|--------------------------|-------------------------------------------------------------------------|
| **Signup Source**        | Highest adoption: Google Auth (17.3%) and Guest Invites (17.1%)         |
|                          | Lowest adoption: Personal Projects (8.1%)                               |
| **Referral (Invited)**   | Invited users had higher adoption (14.7%) vs. non-invited (12.8%)       |
| **Marketing Emails**     | Slightly higher adoption for users opted-in (~14.3% vs. ~13.6%)         |

## Recommendations

- **Promote high-converting signup methods**: Google Auth and Guest Invite
- **Improve low-performing paths**: Personal Projects onboarding needs review
- **Leverage referrals**: Encourage invites, track successful inviters
- **Refine email campaigns**: Test more targeted drip content for different user types

## Limitations & Next Steps

- Time-based features predict adoption but aren’t directly actionable
- Segmenting further by organization or behavior may reveal deeper drivers
- Product usage data beyond logins could improve future models
