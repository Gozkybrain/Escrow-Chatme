# Chat Me 🌍

ChatMe is a comprehensive chat escrow application featuring real-time escrow based p2p trading, and funds management for secure transactions. The app includes user authentication, profile management, escrow chat functionality, and financial operations, designed to provide a seamless communication and transaction experience.

```
Base background-color: #242424;
```

## Admin Perspective
The authentication of the app is simple, the App entry has a switch cse for two primary components; `GetUser.jsx` and `GetAuth.jsx`. If the user is authenticated, the `GetUser.jsx` comes to play with all of its routes, else the later comes in respectively. Thereby making the App totally authenticated all round.


  ## Folder Structure

  The following is an overview of the main folders and files in the project:

`src/`

* `components/`:
Contains the main pages or views of the application like login, registration etc.

* `lib/`:
Contains configuration and utility files.

    * `firebase.js`: Initializes Firebase services, including authentication, Firestore, and storage.

* `pages/`:
Contains reusable React components used throughout the application.

* `styles/`:
Contains CSS files for styling the components and pages.


## Features

* Payment Gateway: This will serve as a method to add funds to the account for real life case scenario.

* Email Services: This will give users notification when certain actions are carried out.


## Escrow Logic

The escrow system ensures secure transactions with the following logic:

1. **HandleSubmit** (`CreateEscrow.jsx`): This function initiates the escrow by deducting the specified amount from the initiator’s balance and creating an escrow record in the database.

2. **HandleCancel** (`EscrowDetails.jsx`): This function refunds the escrow amount to the initiator’s balance if the escrow is canceled. It updates the escrow status to 'canceled' and restores the funds to the initiator.

3. **HandleAccept** (`EscrowDetails.jxs`): This function allows the recipient to accept the escrow, marking it as 'accepted'. It notifies both parties and waits for confirmation from the initiator before the funds are released.

4. **HandleConfirm** (`EscrowDetails.js`): This function confirms the completion of the escrow. Once confirmed by the initiator, it finalizes the transaction by marking it as 'completed' and transfers the funds to the recipient’s balance.

These functions handle the escrow process, managing funds and status updates securely.

`
This project is part of my Experimental Lab
`
