# Meeting notes TSC 2023-06-20 6pm Pacific Time (US)

All interested in GenevaERS development are welcome to join.

## Conference call details

### Zoom Meeting

- https://zoom-lfx.platform.linuxfoundation.org/meeting/95522057563
  - Ask Andrea
    - When users try this link, they get sent here: 
      - https://zoom-lfx.platform.linuxfoundation.org/password-required
    - We think we need to have a link with the password attached 
      - If so, we should change the link on the https://genevers.org site.  

## Administration

## Workbench
- RTC 22844: Workbench does not generate an error when a constant value is missing
- RTC 23075: Compare Utility does not show LR differences
- RTC 23125: Make coding a "Source-Record" view type more user-friendly

## Performance Engine
- RTC 22485: Research using a hashing algorithm rather than a binary search tree
  - Until now, all of our in-memory reference file searches have used a binary search tree that is built at MR95 initialization time. 
  - We are now introducing a search using a hashing algorithm, which has been shown to reduce the CPU time required in many circumstances. 
  - We will continue to use the binary search tree technique for lookups that require effective dates.  
  - Should all other searches use the hashing technique? 
    - If not, why not? 
    - Do the following factors impact our decision? 
      - The size of the key.
      - The size of the record. 
      - The number of records.  
    - Should we consider other search algorithms? 
      - For very small tables, a sequential search might be the most efficient. 
  - Should the choice of algorithm be specified in the Workbench or in the JCL?  
    - If in the JCL, should it be for the whole run or for each table?  
      - A table is specified by the combination of LR, LF, and LP (lookup path)  
  - If we use the hashing technique, the source records don't need to be sorted. 
    - But if we don't sort them, we'd miss out on the ability to detect duplicate keys at table loading time.  (Is this true?)
    - Also, if you specify that you want to use hashing during the Extract Phase, you won't know that fact during the Reference Phase, where we have the checks for duplicate keys and sort sequence, which you would still need to perform for the tables that use binary search trees.  

## Potential users (who may want support)
- LPAR now available on Karl's machine.
- Need read exit for Adabas.

## Demo

## Run-Control Utilities 

## Documentation
- "A document a week, that's all we ask" 

## Infrastructure

## R&D Work

## Conferences 
- Possible presentation at the Winter SHARE conference 

## For next time 
