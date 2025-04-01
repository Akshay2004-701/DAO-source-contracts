
## SMART CONTRACT INFO

- **DAOFactory**: The central contract that enables organizations to create their own DAOs. It deploys and connects the three core components (NFT Membership, Treasury, and Governance). 
- **NFTMembership**: Handles membership through NFTs and: 
  - Issues NFT-based memberships for a fee paid in USDC
  - Maintains the membership list
  - Ensures only members have voting rights
- **Treasury**: Manages the funds of the organization by: 
  - Storing funds contributed by members
  - Processing payments via approved proposals
  - Tracking all financial transactions
- **Governance**: Implements the proposal and voting system where: 
  - Contributors can submit project proposals with milestones
  - Members review and vote on proposals
  - Approved proposals trigger fund transfers from the treasury

## CONTRACT WORKFLOW

1. An organization uses the DAOFactory contract to create a new DAO.
2. The factory deploys three interconnected contracts: 
   - **NFTMembership**: Manages who can participate in the DAO
   - **Treasury**: Handles all financial operations
   - **Governance**: Controls the proposal and voting system
3. **User Workflow**: 
   - New members join by paying a membership fee in USDC to get an NFT
   - Members can deposit additional funds to the treasury
   - Contributors submit proposals for projects with milestones
   - Members vote on proposals
   - Approved proposals trigger payments from the treasury to contributors
4. **Key Interactions**: 
   - **NFTMembership ↔ Governance**: Only NFT holders can vote
   - **Governance ↔ Treasury**: Approved proposals instruct treasury to release funds
   - **NFTMembership ↔ Treasury**: Members can deposit funds
