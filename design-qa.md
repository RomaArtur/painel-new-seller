# Design QA — Solicitar cadastro

- Source visual truth: `C:\Users\Artur\.codex\visualizations\2026\08\25\01a036ad-a4f4-7110-b221-dd6cbb9757d7\new-seller-audit\04-link-confirmation.png`
- Implementation screenshot: `C:\Users\Artur\.codex\visualizations\2026\08\25\01a036ad-a4f4-7110-b221-dd6cbb9757d7\new-seller-audit\07-solicitar-cadastro-editar-dados.png`
- Full-view comparison: `C:\Users\Artur\.codex\visualizations\2026\08\25\01a036ad-a4f4-7110-b221-dd6cbb9757d7\new-seller-audit\08-before-after-solicitar-cadastro.png`
- Focused modal comparison: `C:\Users\Artur\.codex\visualizations\2026\08\25\01a036ad-a4f4-7110-b221-dd6cbb9757d7\new-seller-audit\09-modal-before-after-focus.png`
- State: transportadora selecionada, modal de confirmação aberto, dados revisados após edição.
- Browser viewport: 2560 × 1440 CSS px; reported device pixel ratio 0.75.
- Source and implementation pixels: 5120 × 2880 each. Both captures use the same browser surface and pixel dimensions, so no density resampling was required for comparison.

## Findings

- No actionable P0, P1, or P2 differences remain.
- Fonts and typography: Inter, weights, hierarchy and line wrapping remain consistent with the existing modal.
- Spacing and layout rhythm: the modal preserves its card, padding, radius and button rhythm; removal of the operational URL reduces height without creating empty space.
- Colors and visual tokens: existing TRACKen green, grays, overlay opacity and focus treatment are preserved.
- Image and icon fidelity: no raster imagery was changed; the new action uses the existing Font Awesome icon set.
- Copy and content: the seller-facing action is now “Solicitar cadastro”, CPF/CNPJ replaces the CNPJ-only label, and the editable-data affordance is visible before confirmation. Operational terminology remains unchanged.

## Interaction checks

- CEP search and carrier selection.
- “Solicitar cadastro” from the carrier popup.
- Enter and cancel edit mode.
- Required-field validation and saving updated seller data.
- Automatic request handoff to the operational without a visible URL field.
- Request received by the operational with the edited document.
- Seller success state after submission.
- Console checked: no application JavaScript errors; only the existing Tailwind CDN warning and an Electron sandbox diagnostic from the browser host.

## Comparison history

- Pass 1: the focused before/after comparison confirmed the intended copy and field changes while preserving the existing visual system. No blocking visual fixes were required.

final result: passed
