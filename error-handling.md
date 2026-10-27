# LOAN_API — Error Handling

[← Back to Overview](README.md) · [API Reference](api.md) · [Workflows](workflows.md) · [Data Model](data-model.md) · [Dependencies](dependencies.md) · [Error Handling](error-handling.md)

Only code-visible messages with material business meaning are listed here. Generic exception wrapping and hypothetical Oracle errors are excluded.

| API Method | Observed error / condition | Handling |
|---|---|---|
| [post_int_amount_to_plan](api.md#post-int-amount-to-plan) | `Posting amounts is not allowed for this account type{` | Invokes the package error routine or raises an application error in the shown method path. |
| [get_amount_for_pen_calc](api.md#get-amount-for-pen-calc-1) | `Overdue int in plan or ovd_balance amount for penalty calculation is negative!` | Invokes the package error routine or raises an application error in the shown method path. |
| [get_interest_calc_dates](api.md#get-interest-calc-dates) | `p_int_calc_at param should be EOD or SOD!!` | Invokes the package error routine or raises an application error in the shown method path. |
| [get_interest_calc_dates](api.md#get-interest-calc-dates) | `P_EOD_SOD param should be E - EOD or S - SOD!!` | Invokes the package error routine or raises an application error in the shown method path. |
| [get_interest_calc_dates_ex](api.md#get-interest-calc-dates-ex) | `p_int_calc_at param should be EOD or SOD!!` | Invokes the package error routine or raises an application error in the shown method path. |
| [get_interest_calc_dates_ex](api.md#get-interest-calc-dates-ex) | `P_EOD_SOD param should be E - EOD or S - SOD!!` | Invokes the package error routine or raises an application error in the shown method path. |
| [do_create_tranche](api.md#do-create-tranche) | `p_trn_type should be CREATE - for create, DELETE - for delete` | Invokes the package error routine or raises an application error in the shown method path. |
| [get_voucher_data_from_query](api.md#get-voucher-data-from-query) | `p_result_type should be SINGLE_ROW or MULTI_ROW!` | Invokes the package error routine or raises an application error in the shown method path. |
| [get_voucher_data_from_query](api.md#get-voucher-data-from-query) | `GROUP_CODE field is not defined in query or GROUP_CODE field is null!` | Invokes the package error routine or raises an application error in the shown method path. |
| [loan_int_diff_operation](api.md#loan-int-diff-operation) | `original_amount or residual_amount or calc_amount or sum_residual_amount or p_plan_int_amount or p_int_amount is negative` | Invokes the package error routine or raises an application error in the shown method path. |
| [loan_int_diff_operation](api.md#loan-int-diff-operation) | `Operation type must be INS, OPEN, CLOSE!` | Invokes the package error routine or raises an application error in the shown method path. |
| [get_gl_acc_from_matrix](api.md#get-gl-acc-from-matrix) | `p_gl_base_type should be MAIN - for main account, OVD_MAIN - for overdue account!` | Invokes the package error routine or raises an application error in the shown method path. |
| [get_gl_acc_from_matrix](api.md#get-gl-acc-from-matrix) | `p_acc_type is invalid!` | Invokes the package error routine or raises an application error in the shown method path. |
| [get_ovd_date](api.md#get-ovd-date) | `p_calc_mode should be FOR_PEN_CALC - for penalty calculation, DEFAULT-for reporting` | Invokes the package error routine or raises an application error in the shown method path. |
| [get_ovd_date_old](api.md#get-ovd-date-old) | `p_calc_mode should be FOR_PEN_CALC - for penalty calculation, DEFAULT-for reporting` | Invokes the package error routine or raises an application error in the shown method path. |
| [get_amount_for_pen_calc](api.md#get-amount-for-pen-calc-2) | `p_for_spec_days must be Y or N!` | Invokes the package error routine or raises an application error in the shown method path. |
| [table_log_operation](api.md#table-log-operation) | `Oper type should be LOGGING-for logging or RESTORING-for restoring` | Invokes the package error routine or raises an application error in the shown method path. |
| [table_log_operation](api.md#table-log-operation) | `Table name should be [LOAN_PAYMENT_PLAN],[LOAN_FLOW_RATIO_INFO],[LOAN_STOP_RATIO_INFO],[LOAN_CATEGORY],[KRD_KOM_PLAN_DETAY]` | Invokes the package error routine or raises an application error in the shown method path. |
| [do_journal_entry](api.md#do-journal-entry) | `p_trn_type must be CREATE or POST!` | Invokes the package error routine or raises an application error in the shown method path. |
| [recalculate_int_payment_plan](api.md#recalculate-int-payment-plan) | `p_schedule_update_type should be 3 or 4!` | Invokes the package error routine or raises an application error in the shown method path. |
| [create_loan_history](api.md#create-loan-history) | `p_app_oper_code not found in loan_operation_desc table!` | Invokes the package error routine or raises an application error in the shown method path. |
| [create_loan_history](api.md#create-loan-history) | `p_trn_type must be I-insert, U-update, D-delete` | Invokes the package error routine or raises an application error in the shown method path. |
| [generate_allocated_payment_list](api.md#generate-allocated-payment-list) | `Payment amount cant be negative!` | Invokes the package error routine or raises an application error in the shown method path. |
| [do_Auto_Payment](api.md#do-auto-payment) | `Auto payment type should be 1-Plan payment or 2-Off plan payment!` | Invokes the package error routine or raises an application error in the shown method path. |
| [do_int_calculation](api.md#do-int-calculation) | `Product code not found in pkrd_turkod_pr table, pls check 22401 app for this loan product!` | Invokes the package error routine or raises an application error in the shown method path. |
| [do_int_calculation](api.md#do-int-calculation) | `Interest ratio cant be negative:` | Invokes the package error routine or raises an application error in the shown method path. |
| [do_overdue_transit_operation](api.md#do-overdue-transit-operation) | `Loan product code not found in pkrd_turkod_pr table!` | Invokes the package error routine or raises an application error in the shown method path. |
| [create_overdrafts](api.md#create-overdrafts) | `p_oper_type should be CREATE_OVERDRAFT or CLOSE_LOAN` | Invokes the package error routine or raises an application error in the shown method path. |
| [init_global_variables](api.md#init-global-variables) | `[krd_teklif_detay] is invalid` | Invokes the package error routine or raises an application error in the shown method path. |
| [init_global_variables](api.md#init-global-variables) | `[krd_teklif] is invalid` | Invokes the package error routine or raises an application error in the shown method path. |
| [UPDATE_PAYMENT_PLAN](api.md#update-payment-plan) | `This operation cannot be initialized when [with_tranche_info_yn] =` | Invokes the package error routine or raises an application error in the shown method path. |

## Important constraints

- `r(...)` is a package-local error routine call in the source. Its implementation is not independently established by the supplied public specification.
- Deliberate propagation, rollback, and explicit `COMMIT` behavior must be confirmed on the specific call path; do not assume all methods are autonomous or self-committing.

