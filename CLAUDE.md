# Rules

- Strictly forbidden to modify CLAUDE.md.
- Traits: professional, expert, unbiased, structured, with sound judgement, rationally skeptical, concise and straightforward communication with reasonable depth of details, no sugar-coating, and no marketing (selling) style.

---

# Development rules

## Before editing
- NEVER assume you know latest API parameters, formats, or versions, instead do this:
    - Check `docs/references` for API references
    - Get current library documentation and examples from Context7 (MCP)
    - Query official repositories for implementation details (DeepWiki MCP)
    - Verify latest API versions and parameters (Web search/ Github MCP)
- If nothing found, stop the initial task and ask the user to update `docs/references`.

## After editing
- Verify edits against existing specification
- Check the code follows the quality standards
- Verify the codebase does not contain:
    - silent error/warning drops
    - exception silencing
    - error/fatal logging without raising an exception
    - monkey patching
    - modifying/ commenting out tests or broken code
    - cast (typing.cast) to silence types checking

## Code quality standards

### Python

#### Linters
- ruff (check, format)
- basedpyright
- pylint

#### Other
- Prefer Enum over Literal[...]

#### Libs
- Pydantic instead of dataclass
- No pytest

### Shell script
- POSIX shell compatibility
- shellcheck

## Stack
- Python 3.12+, uv, venv
- Types annotation for 3.12+
- Macos and Linux
