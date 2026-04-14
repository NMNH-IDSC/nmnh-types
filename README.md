# NMNH Type Counts

Type counts are based on the Type Citations table in the EMu Catalog module. Each
catalog record can include one or more type statuses, and each row is counted
separately. This means that the number of types may exceed the number of type
records in EMu.

Counts are based on guidance for type nomenclature provided by the ICZN (for animals)
and ICN (for plants). Please see types.csv for how each status is handled, including
mappings for primary and secondary statuses. Note that two unofficial statuses
(type and cotype) are treated as primary types for this report. 

Terms in the Type Status field in EMu are not standardized. The following variants
are mapped to the standard version of each type status:

- Plurals (like "cotypes")
- Multiples (like "holotype + allotype")
- Fragments, parts, and collections (like "part of holotype" or "type collection")
- Uncertain statuses (like "possible syntype" or "neotype?")

Unoffocial compound statuses (like "paraneotype") could not be mapped to official
values but are counted as secondary types. The exact mapping for each status,
including unmapped terms, can be found on the nmnh-type-counts.xlsx spreadsheet.

By default, all statuses that can be mapped are counted.

A small number of terms require further evaluation, including:

- clastotype
- clonotype
- morphotype
- phototype (plus related terms using the photo- prefix)
- plastotype (plus related terms using the plasto- prefix)
- topotype

## nmnh-type-counts metadata

- **counts** includes counts for the full collection
- **total_by_dept** includes counts for all types for each department
- **primary_by_dept** includes counts for primary types for each department
- **secondary_by_dept** includes counts for secondary types for each department
- **data** includes the mapping and counts for each distinct term in Type Status
- **match_types** includes counts for each different match type
    - *backlog* means the count was estimated from a departmental backlog
    - *compound* means the status includes multiple valid prefixes
    - *exact* means the status exactly matches a known term
    - *modified* means the status can be mapped to a known term by removing terms
      like primary, collection, etc.
    - *part* means the status can be mapped to a known term by removing terms
      like "part of" or "fragment"
    - *uncertain* means the status includes an uncertainty modifier like "possible"
    - *--* means the status could not be mapped

    