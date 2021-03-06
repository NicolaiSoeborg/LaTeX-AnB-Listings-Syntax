# LaTeX (Listings) syntax for AnB

## Syntax

```tex
\lstdefinelanguage{AnB}{
  keywords=[1]{Agent, Number, Function, Symmetric_key, PublicKey},
  keywords=[2]{Protocol, Types, Knowledge, Goals, Actions},
  keywords=[3]{section, inits, rules, step, initial_state, attack_state, not, where, authenticates, on, secret, between},
  keywordstyle=[1]\color{violet},
  keywordstyle=[2]\color{magenta},
  keywordstyle=[3]\bf,
  sensitive=false, % keywords are not case-sensitive
  morecomment=[l]{\#}, % line comment
  morecomment=[l]{\%}, % line comment
  %morecomment=[s]{/*}{*/}, % start and end delimiter
  basicstyle=\footnotesize,
  literate=%
    {->}{\begingroup{\color{blue}$\rightarrow$}\endgroup}2%
    {\{}{\begingroup{\color{blue}\{}\endgroup}1%
    {\}}{\begingroup{\color{blue}\}}\endgroup}1%
    % Catch {|  |}  s.t. we can add them to a math env. = less space between chars
    {\{|}{\begingroup{\color{red}$\{\vert$}\endgroup}2%
    {|\}}{\begingroup{\color{red}$\vert\}$}\endgroup}2%
    {*}{$\bullet$}1,
}
```

## Example

![Example of an image w/ a AnB listing](example.png)
