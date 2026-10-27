# LOAN_API — Dependencies

[← Back to Overview](README.md) · [API Reference](api.md) · [Workflows](workflows.md) · [Data Model](data-model.md) · [Dependencies](dependencies.md) · [Error Handling](error-handling.md)

Dependencies below are names of directly invoked packages/modules in the supplied Body; they are not a verified inventory of all transitive integrations.

| Dependency | Kind | Verified use | Used by |
|---|---|---|
| `APEX_KRD2204_0_API_P` | Referenced PL/SQL module | Direct routine call in implementation | [do_create_tranche](api.md#do-create-tranche), [do_Auto_Payment](api.md#do-auto-payment) |
| `APEX_KRD2204_2_API_P` | Referenced PL/SQL module | Direct routine call in implementation | [do_Auto_Payment](api.md#do-auto-payment) |
| `APEX_KRD2204_7_API_P` | Referenced PL/SQL module | Direct routine call in implementation | [do_Auto_Payment](api.md#do-auto-payment) |
| `APEX_KRD2220_0_API_P` | Referenced PL/SQL module | Direct routine call in implementation | [do_guarantee_out](api.md#do-guarantee-out), [do_non_cash_loan_close](api.md#do-non-cash-loan-close) |
| `API_CALENDAR` | Referenced PL/SQL module | Direct routine call in implementation | [UPDATE_PAYMENT_PLAN](api.md#update-payment-plan) |
| `API_VISTA` | Referenced PL/SQL module | Direct routine call in implementation | [create_overdrafts](api.md#create-overdrafts) |
| `BLOKE_API` | Referenced PL/SQL module | Direct routine call in implementation | [do_loan_collateral_out](api.md#do-loan-collateral-out) |
| `CL` | Referenced PL/SQL module | Direct routine call in implementation | [do_overdue_transit_operation](api.md#do-overdue-transit-operation) |
| `CR` | Referenced PL/SQL module | Direct routine call in implementation | [do_overdue_transit_operation](api.md#do-overdue-transit-operation) |
| `GAIA` | Referenced PL/SQL module | Direct routine call in implementation | [UPDATE_PAYMENT_PLAN](api.md#update-payment-plan) |
| `GLBL` | Referenced PL/SQL module | Direct routine call in implementation | [loan_int_diff_operation](api.md#loan-int-diff-operation), [get_plan_error](api.md#get-plan-error), [do_loan_control](api.md#do-loan-control-2) |
| `GLBL_BAKIYE` | Referenced PL/SQL module | Direct routine call in implementation | [do_Auto_Payment](api.md#do-auto-payment), [do_commission_recognition](api.md#do-commission-recognition), [do_guarantee_out](api.md#do-guarantee-out), [do_non_cash_loan_close](api.md#do-non-cash-loan-close) |
| `GLBL_CCY` | Referenced PL/SQL module | Direct routine call in implementation | [do_loan_collateral_out](api.md#do-loan-collateral-out), [do_Auto_Payment](api.md#do-auto-payment) |
| `GLBL_EOD` | Referenced PL/SQL module | Direct routine call in implementation | [do_loan_collateral_out](api.md#do-loan-collateral-out), [do_Loan_Close_With_Collateral_Out](api.md#do-loan-close-with-collateral-out) |
| `GLBL_FAIZ` | Referenced PL/SQL module | Direct routine call in implementation | [get_commission_schedule](api.md#get-commission-schedule), [get_amount_for_pen_calc](api.md#get-amount-for-pen-calc-2), [get_Plan_Month_Count](api.md#get-plan-month-count), [get_Pym_Startdate](api.md#get-pym-startdate) and more |
| `GLBL_FUNCTIONS` | Referenced PL/SQL module | Direct routine call in implementation | [do_journal_entry](api.md#do-journal-entry) |
| `GLBL_HESAP` | Referenced PL/SQL module | Direct routine call in implementation | [evaluate_limit_amount](api.md#evaluate-limit-amount), [get_gl_acc_from_matrix](api.md#get-gl-acc-from-matrix), [do_journal_entry](api.md#do-journal-entry), [get_new_acc](api.md#get-new-acc) and more |
| `GLBL_NAME` | Referenced PL/SQL module | Direct routine call in implementation | [create_account](api.md#create-account) |
| `GLBL_TARIH` | Referenced PL/SQL module | Direct routine call in implementation | [get_interest_calc_dates](api.md#get-interest-calc-dates), [get_interest_calc_dates_ex](api.md#get-interest-calc-dates-ex), [get_commission_schedule](api.md#get-commission-schedule), [get_Pym_Startdate](api.md#get-pym-startdate) and more |
| `GLOG` | Referenced PL/SQL module | Direct routine call in implementation | [do_com_schedule_allignment](api.md#do-com-schedule-allignment) |
| `GNI_MESSAGE` | Referenced PL/SQL module | Direct routine call in implementation | [get_commission_schedule](api.md#get-commission-schedule), [get_Pym_Startdate](api.md#get-pym-startdate), [create_account](api.md#create-account), [get_new_acc](api.md#get-new-acc) and more |
| `GNI_UTILITY` | Referenced PL/SQL module | Direct routine call in implementation | [do_loan_control](api.md#do-loan-control-1), [do_Auto_Payment](api.md#do-auto-payment), [do_int_calculation](api.md#do-int-calculation), [do_overdue_transit_operation](api.md#do-overdue-transit-operation) |
| `KRD2204_0_API` | Referenced PL/SQL module | Direct routine call in implementation | [do_create_tranche](api.md#do-create-tranche), [do_Auto_Payment](api.md#do-auto-payment) |
| `KRD2220_0_API` | Referenced PL/SQL module | Direct routine call in implementation | [do_guarantee_out](api.md#do-guarantee-out), [do_non_cash_loan_close](api.md#do-non-cash-loan-close) |
| `KRD_EOD` | Referenced PL/SQL module | Direct routine call in implementation | [do_delete_operation](api.md#do-delete-operation), [do_commission_recognition](api.md#do-commission-recognition) |
| `LA` | Referenced PL/SQL module | Direct routine call in implementation | [do_int_calculation](api.md#do-int-calculation) |
| `LOAN_CATEGORY_API` | Referenced PL/SQL module | Direct routine call in implementation | [change_account_status](api.md#change-account-status) |
| `LOAN_REPORT_API` | Referenced PL/SQL module | Direct routine call in implementation | [evaluate_limit_amount](api.md#evaluate-limit-amount), [do_int_calculation](api.md#do-int-calculation), [do_overdue_transit_operation](api.md#do-overdue-transit-operation) |
| `LOAN_TRANCHE_API` | Referenced PL/SQL module | Direct routine call in implementation | [post_int_amount_to_plan](api.md#post-int-amount-to-plan), [finalize_addtional_process](api.md#finalize-addtional-process), [do_create_tranche](api.md#do-create-tranche), [do_delete_operation](api.md#do-delete-operation) and more |
| `MM_ACCOUNTING#` | Referenced PL/SQL module | Direct routine call in implementation | [do_delete_operation](api.md#do-delete-operation), [do_journal_entry](api.md#do-journal-entry), [do_loan_collateral_out](api.md#do-loan-collateral-out) |
| `O` | Referenced PL/SQL module | Direct routine call in implementation | [get_loan_amount](api.md#get-loan-amount), [generate_allocated_payment_list](api.md#generate-allocated-payment-list), [add_payment_details](api.md#add-payment-details) |
| `P` | Referenced PL/SQL module | Direct routine call in implementation | [get_loan_amount](api.md#get-loan-amount), [generate_allocated_payment_list](api.md#generate-allocated-payment-list) |
| `PA_API#` | Referenced PL/SQL module | Direct routine call in implementation | [do_journal_entry](api.md#do-journal-entry), [do_loan_collateral_out](api.md#do-loan-collateral-out) |
| `PH_API` | Referenced PL/SQL module | Direct routine call in implementation | [do_loan_collateral_out](api.md#do-loan-collateral-out) |
| `PR` | Referenced PL/SQL module | Direct routine call in implementation | [do_int_calculation](api.md#do-int-calculation) |
| `RUHA3H` | Referenced PL/SQL module | Direct routine call in implementation | [clear_addtional_data](api.md#clear-addtional-data), [add_additional_group](api.md#add-additional-group), [add_additional_info](api.md#add-additional-info-1), [add_column_update](api.md#add-column-update-1) |
| `TRN_BROKER` | Referenced PL/SQL module | Direct routine call in implementation | [do_journal_entry](api.md#do-journal-entry), [create_loan_history](api.md#create-loan-history), [do_loan_collateral_out](api.md#do-loan-collateral-out), [do_guarantee_out](api.md#do-guarantee-out) and more |

## Operational considerations

- Transaction identifiers, dates, GL/account mapping and EOD/SOD parameters are caller-visible prerequisites on relevant methods.
- Unprovided definitions of the called modules mean their internal behavior cannot be determined from these files.

