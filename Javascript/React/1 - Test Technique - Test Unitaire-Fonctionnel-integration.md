# Test Technique pour un Développeur JavaScript / React
Bienvenue dans ce test technique. L'objectif est d'évaluer vos compétences en JavaScript, en particulier avec React, ainsi que votre capacité à écrire différents types de tests : unitaires, fonctionnels et d'intégration. Vous aurez à développer une petite application React et à y ajouter les tests appropriés.

## Contexte
Vous devez créer une petite application de gestion de tâches (To-Do List). L'application doit permettre de :

1. Ajouter une tâche.
2. Marquer une tâche comme terminée.
3. Supprimer une tâche.
4. Afficher la liste des tâches.

## Instructions
1. Créer l'application React :
- Utilisez create-react-app pour initialiser votre projet.
- Développez les composants nécessaires pour les fonctionnalités décrites ci-dessus.
- Utilisez un état local (state) pour gérer la liste des tâches.

2. Écrire les tests unitaires :
- Utilisez Jest pour écrire des tests unitaires.
- Testez les fonctions qui ajoutent, marquent comme terminées, et suppriment les tâches.
- Par exemple, testez une fonction addTask pour vérifier qu'elle ajoute correctement une tâche à la liste.

3. Écrire les tests fonctionnels :
- Utilisez React Testing Library pour écrire des tests fonctionnels.
- Testez l'interface utilisateur pour vérifier que les boutons et les interactions fonctionnent comme prévu.
- Par exemple, testez si cliquer sur le bouton "Ajouter" ajoute une tâche à la liste affichée.

4. Écrire les tests d'intégration :
- Écrivez des tests d'intégration pour vérifier que les différents composants fonctionnent bien ensemble.
- Par exemple, testez un scénario où une tâche est ajoutée, marquée comme terminée, puis supprimée, et vérifiez que l'état de l'application est correct à chaque étape.

## Détails Techniques
### Structure du Projet :

```java
my-todo-app/
├── public/
├── src/
│   ├── components/
│   │   ├── TaskList.js
│   │   ├── TaskItem.js
│   │   └── AddTaskForm.js
│   ├── App.js
│   ├── index.js
│   └── __tests__/
│       ├── App.test.js
│       ├── TaskList.test.js
│       ├── TaskItem.test.js
│       └── AddTaskForm.test.js
├── package.json
└── README.md
```

### Fonctionnalités à implémenter :
- AddTaskForm.js : Composant pour ajouter une tâche.
- TaskList.js : Composant pour afficher la liste des tâches.
- TaskItem.js : Composant pour afficher une tâche individuelle avec des boutons pour marquer comme terminé et supprimer.

## Exemple de Tests
### Test Unitaire pour addTask :

```javascript
// src/__tests__/App.test.js
import { addTask } from '../App';

test('addTask adds a new task to the list', () => {
  const initialTasks = [];
  const newTask = { id: 1, text: 'Learn React', completed: false };
  const updatedTasks = addTask(initialTasks, newTask);

  expect(updatedTasks).toHaveLength(1);
  expect(updatedTasks).toContainEqual(newTask);
});
```

### Test Fonctionnel pour le bouton d'ajout :

```javascript
// src/__tests__/AddTaskForm.test.js
import { render, screen, fireEvent } from '@testing-library/react';
import AddTaskForm from '../components/AddTaskForm';

test('renders AddTaskForm and adds a task', () => {
  render(<AddTaskForm />);
  const input = screen.getByPlaceholderText(/add a new task/i);
  const button = screen.getByText(/add task/i);

  fireEvent.change(input, { target: { value: 'Learn React' } });
  fireEvent.click(button);

  const task = screen.getByText(/learn react/i);
  expect(task).toBeInTheDocument();
});
```
### Test d'Intégration pour le cycle complet :

```javascript
// src/__tests__/App.test.js
import { render, screen, fireEvent } from '@testing-library/react';
import App from '../App';

test('full app integration test', () => {
  render(<App />);
  const input = screen.getByPlaceholderText(/add a new task/i);
  const addButton = screen.getByText(/add task/i);

  // Add a task
  fireEvent.change(input, { target: { value: 'Learn React' } });
  fireEvent.click(addButton);
  expect(screen.getByText(/learn react/i)).toBeInTheDocument();

  // Mark task as completed
  const completeButton = screen.getByText(/complete/i);
  fireEvent.click(completeButton);
  expect(screen.getByText(/learn react/i)).toHaveClass('completed');

  // Delete task
  const deleteButton = screen.getByText(/delete/i);
  fireEvent.click(deleteButton);
  expect(screen.queryByText(/learn react/i)).not.toBeInTheDocument();
});
```

## Soumission
- Clonez ce dépôt GitHub.
- Implémentez les fonctionnalités et les tests requis.
- Assurez-vous que tous les tests passent.
- Soumettez le lien vers votre dépôt GitHub avec votre solution.

Bonne chance ! Nous attendons avec impatience de voir votre travail.






