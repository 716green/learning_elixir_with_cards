# Cards

## Setup - Setup and Run

`/{project_name}/lib/{project_name}.ex`

```shell
# Compile in Interactive Elixir shell
iex -S mix

# Recompile app
recompile
```

## Functions

`create_deck` - Create an array of playing cards
`shuffle` - Shuffle an array of playing cards
`deal` - Create a 'hand' of cards
`contains?` - Given a deck and a single card, figure out if the card is in the deck
`save` - Save a collection of cards to a file on the local machine
`load` - Load a collection of cards from the local machine

---

## Variables

Variables are assigned simply as `deck = Cards.create_deck`

## Methods

Methods that return boolean values have a ? in the name by convention

## Pattern Matching

```elixir
color1 = ["red"]
color1 #= ["red"]

[color2] = ["red"]
color2 #= "red"
```

## Maps

```elixir
colors = %{primary: "red", secondary: "blue"}
colors.primary # "red"
colors.secondary # "blue"
%{secondary: secondary_color} = colors
secondary_color # "blue"

# Creates a new map
Map.put(colors, :primary, "green")

%{ colors | primary: "blue" }

# This can not be used to add a new value, only update
%{ colors | secondary_color: "yellow" }
```

## Keyword Lists

```elixir
colors = [{:primary, "red"}, {:secodary: "green"}]
colors[:primary] # "red"
```

## Installation

If [available in Hex](https://hex.pm/docs/publish), the package can be installed
by adding `cards` to your list of dependencies in `mix.exs`:

```elixir
def deps do
  [
    {:cards, "~> 0.1.0"}
  ]
end
```

Documentation can be generated with [ExDoc](https://github.com/elixir-lang/ex_doc)
and published on [HexDocs](https://hexdocs.pm). Once published, the docs can
be found at <https://hexdocs.pm/cards>.
