https://forum.obsidian.md/t/dataview-list-of-files-as-checklist/44807

```dataview
TASK 
FROM (#pantry)
WHERE !completed 
```
[]][[]]
To create a checklist in Obsidian using Dataview, you can use theÂ `TASK`Â query type to generate an interactive list of tasks, which can function as a checklist. This is particularly useful for managing to-do items that are marked with a checkbox syntax (e.g.,Â `- [ ] Task`) in your notes.Â For example, a basic query to list all incomplete tasks is:

```
TASK WHERE !completed
```

This will display all unchecked tasks from your vault as an interactive checklist, and checking a task in the Dataview block will automatically update the original note.Â You can refine this further by filtering tasks based on tags, due dates, or specific file locations. For instance, to list incomplete tasks with a specific tag likeÂ `#shopping`, use:

```
TASK WHERE !completed AND contains(tags, "#shopping")
```

If you want to list tasks from specific headings within a note, you can use theÂ `econtains`Â function combined withÂ `meta(header).subpath`Â to target tasks under specific section headings, such as "Brain Dump" or "6 Priorities".Â For example:

```
TASK WHERE econtains(list("Brain Dump", "6 Priorities", "Life", "Family", "Work", "Health"), meta(header).subpath) AND !completed
```

This query retrieves all incomplete tasks located under the specified headings across your notes.Â You can also group tasks by their originating file usingÂ `GROUP BY file.link`, which helps organize your checklist by source note.Â Additionally, you can useÂ `LIST`Â orÂ `TABLE`Â query types to display tasks or other

- [ ] ## extra
- Pagels book
- gifts for Scott
- check on delivery Wednesday
- [ ] Strength chord
## clothes

- [ ] semi-formal
- [ ] sleep
- [ ] lounge
- biking shoes

## bathroom

- [ ] cf. previous 

## tech

- [ ] hearing aids
- [ ] which computer? charger
- [ ] bedside cords
- bike stuff: stool, front bag, helmet, pump
- tablet, e-screen, acer, phone
- journal

## kitchen

- coffee & filters
- wine & cork screw
- snacks
- cooling pack for mounjaro
- cooling pack for cooler
- cheese sticks
- hard-boiled eggs?
- cheese
- trail mix
 data in different formats, butÂ `TASK`Â is specifically designed for interactive checklists