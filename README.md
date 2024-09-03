# Project Planning with Gantt Charts

## Overview

This project demonstrates how to create and visualise a Gantt chart using Python. The primary objective is to help project managers, developers, and teams visually plan and track the progress of their data science projects using a simple and interactive Gantt chart.

The project includes:
1. A script to load tasks from a CSV file.
2. A function to generate a Gantt chart with progress visualisation.
3. Detailed tooltips for each task, showing start and end dates, progress, and descriptions.
4. A prompt example for chat bots to streamline the project planning process.
5. A manual template for those who prefer to plan their projects manually.

## Getting Started

### Prerequisites

To run this project, you need to have Python installed along with the following libraries:
- `pandas`
- `plotly`

You can install the necessary libraries using pip:

```bash
pip install pandas plotly
```

### Project Structure

- **`project_planning.py`**: The main script to create and visualize the Gantt chart.
- **`resources/template.csv`**: A CSV template that can be used to input tasks.
- **`README.md`**: Documentation and instructions for using this project.

### Using the Project

#### **Option 1: Prompt Assisted Project Planning**

To streamline your project planning process, you can use the provided prompt with a chat bot. This method ensures that your plan follows best practices for project management by including all necessary stages and tasks.

**Sample Chat Bot Prompt:**

```
I am starting a project and need help with planning it from ideation to deployment. The project duration is [X] weeks, and the project is about [brief description of the project].

Please help me outline the key phases, tasks, and milestones over this period. Break the project down into logical weekly sections, and include specific tasks for each week. Each task should be a distinct action or sub-task relevant to the weekly goal, providing a clear and detailed description of what needs to be accomplished. Ensure the plan follows best practices for project management.

The final output should be structured in a CSV format with the following columns:

Task: Each task should be labeled as 'Week X: Task Y', where X is the week number and Y is the task number within that week.
Start: The start date of the task (YYYY-MM-DD).
Finish: The end date of the task (YYYY-MM-DD).
Progress: The progress percentage (0 to 100, initially 0%).
Description: A detailed description of what the task entails, focusing on specific actions or sub-tasks.
Please ensure the tasks are evenly distributed across the weeks and cover all aspects of the project, from initial planning to final deployment and post-launch review. Provide the output in a CSV format.
```

#### **Option 2: Manual Project Planning**

If you prefer to plan manually, a template has been provided. You can fill out the template in a spreadsheet or a text editor. Once you have finalised your tasks, save the file as a `.csv` file for use in the project; noting the file path for use in the scripting notebook.

### Loading Tasks and Creating the Gantt Chart

1. **Define Your Project**: Start by defining your project in a CSV file. Use the template provided in `resources/template.csv`.

2. **Load Tasks**: The script loads tasks from the CSV file you specify. Ensure your CSV file has the following columns:
   - `Task`: A brief description of the task.
   - `Start`: The start date in `YYYY-MM-DD` format.
   - `Finish`: The end date in `YYYY-MM-DD` format.
   - `Progress`: The completion percentage (0 to 100).
   - `Description`: A detailed description of what the task entails.

3. **Run the Script**: Execute the script by running:

    ```bash
    python project_planning.py
    ```

    You will be prompted to enter the path to your CSV file. Once entered, the script will generate a Gantt chart based on your input.

4. **View the Gantt Chart**: The chart will be displayed in your default web browser, showing the tasks, their timelines, and progress.

### Example Usage

```python
python project_planning.py
```

**Sample CSV Data:**
```csv
Task,Start,Finish,Progress,Description
Week 1: Task 1,2024-09-01,2024-09-07,20,Define project objectives and scope. Finalize key deliverables and stakeholders.
Week 2: Task 1,2024-09-08,2024-09-14,0,Conduct initial research on existing image analysis tools and technologies.
...
```

### Customisation

You can customize the following:
- **Color Scale**: Modify the `color_continuous_scale` in the `create_gantt_chart` function to use different color schemes.
- **Hover Information**: Add or remove details from the hover tooltip by editing the `hovertemplate`.
- **Annotations**: If you prefer annotations instead of tooltips, you can re-enable or adjust them in the chart.

## Author

This project was created by **Wendy Ware**.

- LinkedIn: [Your LinkedIn Profile](https://www.linkedin.com/in/yourprofile)
- GitHub: [Whereiswendy](https://github.com/Whereiswendy)
- Email: [your-email@example.com](mailto:your-email@example.com)

## Contributing

Contributions are welcome! If you have any suggestions or improvements, feel free to fork the repository and submit a pull request.

## License

This project is licensed under the MIT License - see the `LICENSE.md` file for details.

## Acknowledgments

- Thanks to the developers of `pandas` and `plotly` for providing powerful tools to work with data and visualisation.
- Inspired by the need for simple and effective project management tools in Python.
