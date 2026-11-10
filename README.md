# Community Learning Center Management System

Short Description

The Community Learning Center Management System is an interactive, console-based Dart application designed to manage learning center resources and participants. The application allows users to register learning resources (books, media, etc.) and participants, track borrowing and returning workflows, enforce system rules, and view real-time inventory and registration statistics.



Features Implemented

* Interactive Command-Line Interface (CLI): A loop-driven menu providing real-time user selection for managing resources, participants, and transactions.
* Input Validation & Error Handling:** Prevents duplicate record IDs, missing or empty fields, and invalid menu choices using robust logical checks and `try-catch` blocks.
* Collection-Based Management: Uses Dart `List` and `Map` collections to handle linear iterations for report generation and $O(1)$ constant-time key lookups for transaction operations[cite: 1].
* Encapsulation: Protects internal data representation (`_id`, `_name`) using private variable scoping, getters, and controlled validation setters[cite: 1].
* Object-Oriented Design & Hierarchy:
  * Abstract Base Class (`CenterRecord`):  Establishes common properties (`_id`, `_name`) and forces implementation of the abstract `displayDetails()` method[cite: 1].
  * Concrete Subclasses (`LearningResource` & `Participant`): Inherit from the base class and implement customized detail displays[cite: 1].
  * Mixin Integration (`TimestampMixin`): Modularly adds timestamp capabilities to attach a creation date (`createdAt`) to records upon instantiation[cite: 1].
  * **Polymorphism:** Iterates over base class references (`CenterRecord`) inside the record viewing functionality to dynamically invoke appropriate subclass display logic[cite: 1].



Instructions for Running the Program

Option 1: Running via DartPad (Web)
1. Open [DartPad](https://dartpad.dev/) in any modern web browser.
2. Ensure the language selected is Dart.
3. Copy all code from `main.dart` and paste it into the editor window.
4. Click Run and interact with the application using the console panel on the right.

Option 2: Running via Dart SDK (Local Command Line)
1. Ensure the [Dart SDK](https://dart.dev/get-dart) is installed on your local machine.
2. Clone the repository and navigate into the root directory:
   ```bash
   
   cd MD_Midterm_[Surname]_[Section]
