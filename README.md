# Cache mode CI fixture

Unchanged GitHub Actions fixture for the documented
[`cache-mode`](https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-syntax#cache-mode)
workflow and job keys.

The `seed` job inherits workflow-level `write` access and uses the official
separate `actions/cache/restore` and `actions/cache/save` actions. The `verify`
job overrides the mode to `read`, restores the same entry, verifies its bytes,
and confirms that an `always()` save step does not fail when writes are denied.

The immutable action revisions are `actions/checkout` v6 and `actions/cache`
v4.3.0. No credentials or secret cache content are used.
