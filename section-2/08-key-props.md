## Key Props

- Special prop that we use to tell the diffing alghorithm that an element is unique
- Allows React to distinguish between multiaple instances of the same component typee
- When a key stays the same across renders, the element will be kept in the DOM (even if the podition in the tree changes)

  1. Using key in Lists

- When a key changes between renders, the element will be destroyed and new one will be created (even if the position in the tree is the same as before)

  2. Using key to rest state

```jsx
function Tabbed({ content }) {
  const [activeTab, setActiveTab] = useState(0);

  return (
    <div>
      <div className="tabs">
        <Tab num={0} activeTab={activeTab} onClick={setActiveTab} />
        <Tab num={1} activeTab={activeTab} onClick={setActiveTab} />
        <Tab num={2} activeTab={activeTab} onClick={setActiveTab} />
        <Tab num={3} activeTab={activeTab} onClick={setActiveTab} />
      </div>

      {activeTab <= 2 ? (
        <TabContent
          item={content.at(activeTab)}
          key={content.at(activeTab).summary}
        />
      ) : (
        <DifferentContent />
      )}
    </div>
  );
}
```

key is make any instance unique

[Next: reseting state with props](./09-resetting-state-with-props.md)
