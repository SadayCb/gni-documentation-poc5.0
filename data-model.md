# LOAN_API — Data Model

[← Back to Overview](README.md) · [API Reference](api.md) · [Workflows](workflows.md) · [Data Model](data-model.md) · [Dependencies](dependencies.md) · [Error Handling](error-handling.md)

Object mentions reflect direct SQL text in the supplied Body; they do not establish schema constraints or data ownership. Dynamic SQL and called-package internals may not be included.

## Directly referenced data objects

| Object | Verified access | Used by |
|---|---|---|
| `ACTIONS.` | UPDATE | [create_loan_history](api.md#create-loan-history) |
| `CARDS_ALL` | SELECT / UPDATE | [evaluate_limit_amount](api.md#evaluate-limit-amount), [create_overdrafts](api.md#create-overdrafts) |
| `CREATE_SCHEDULE_PARAMETRS` | SELECT | [get_created_schedule](api.md#get-created-schedule) |
| `CS_ACCOUNT` | SELECT / UPDATE | [evaluate_limit_amount](api.md#evaluate-limit-amount), [get_loan_amount](api.md#get-loan-amount), [get_gl_acc_from_matrix](api.md#get-gl-acc-from-matrix), [get_ovd_date](api.md#get-ovd-date) and more |
| `EOD_PROGRAMS_EXCEPTION` | SELECT | [do_Auto_Payment](api.md#do-auto-payment), [do_int_calculation](api.md#do-int-calculation), [create_overdrafts](api.md#create-overdrafts) |
| `GAIA.CS_ACCOUNT` | SELECT | [get_ovd_date](api.md#get-ovd-date) |
| `GAIA.KRD_TEKLIF_DETAY` | SELECT / UPDATE | [UPDATE_PAYMENT_PLAN](api.md#update-payment-plan) |
| `GAIA.KRD_TESIS` | UPDATE | [UPDATE_PAYMENT_PLAN](api.md#update-payment-plan) |
| `GAIA.LOAN_CATEGORY` | SELECT | [evaluate_limit_amount](api.md#evaluate-limit-amount) |
| `GAIA.LOAN_OPERATION_HISTORY` | SELECT | [evaluate_limit_amount](api.md#evaluate-limit-amount) |
| `GAIA.LOAN_PAYMENT_PLAN` | SELECT | [get_ovd_trs_oper_type](api.md#get-ovd-trs-oper-type) |
| `GLBL_TRANSACTION` | SELECT / UPDATE | [do_create_tranche](api.md#do-create-tranche), [do_delete_operation](api.md#do-delete-operation), [create_loan_history](api.md#create-loan-history) |
| `GL_ACCOUNT_DEFINE` | SELECT | [get_gl_acc_active_passive](api.md#get-gl-acc-active-passive) |
| `GL_JOURNAL_LINES` | SELECT | [do_delete_operation](api.md#do-delete-operation), [create_loan_history](api.md#create-loan-history), [update_loan_history](api.md#update-loan-history) |
| `GL_URUN_HESAP_PR` | SELECT | [get_gl_acc_from_matrix](api.md#get-gl-acc-from-matrix) |
| `IBS.ONLINE_CRD_BLOCK` | SELECT / UPDATE | [UPDATE_PAYMENT_PLAN](api.md#update-payment-plan) |
| `KRD_FON_VERILME` | UPDATE | [do_Loan_Close_With_Collateral_Out](api.md#do-loan-close-with-collateral-out) |
| `KRD_GUARANTEE_MAIN` | SELECT | [get_amount_for_pen_calc](api.md#get-amount-for-pen-calc-1) |
| `KRD_KOM_EOD` | INSERT / SELECT / UPDATE | [do_commission_recognition](api.md#do-commission-recognition) |
| `KRD_KOM_PLAN_DETAY` | DELETE / INSERT / SELECT / UPDATE | [table_log_operation](api.md#table-log-operation), [do_commission_recognition](api.md#do-commission-recognition), [do_com_schedule_allignment](api.md#do-com-schedule-allignment) |
| `KRD_KOM_PLAN_DETAY_LOG` | DELETE / INSERT / SELECT | [table_log_operation](api.md#table-log-operation) |
| `KRD_ODEME_PLAN` | SELECT | [init_global_variables](api.md#init-global-variables) |
| `KRD_SCOR_AUTO_C` | SELECT / UPDATE | [do_loan_collateral_out](api.md#do-loan-collateral-out) |
| `KRD_SCOR_EMANET_C` | SELECT / UPDATE | [do_loan_collateral_out](api.md#do-loan-collateral-out) |
| `KRD_SCOR_ESYA_C` | SELECT / UPDATE | [do_loan_collateral_out](api.md#do-loan-collateral-out) |
| `KRD_SCOR_MAIN` | SELECT | [get_account_feature](api.md#get-account-feature), [is_online_offer](api.md#is-online-offer) |
| `KRD_SCOR_ODEME_PLAN` | SELECT | [get_schedule_from_memo](api.md#get-schedule-from-memo) |
| `KRD_SCOR_QARANT_C` | SELECT / UPDATE | [do_loan_collateral_out](api.md#do-loan-collateral-out) |
| `KRD_SCOR_REAL_ESTATE_C` | SELECT / UPDATE | [do_loan_collateral_out](api.md#do-loan-collateral-out) |
| `KRD_SCOR_SEHMLER_C` | SELECT / UPDATE | [do_loan_collateral_out](api.md#do-loan-collateral-out) |
| `KRD_SCOR_TEMINAT_ALAKA_C` | SELECT / UPDATE | [do_loan_collateral_out](api.md#do-loan-collateral-out) |
| `KRD_SCOR_ZAMIN_C` | SELECT / UPDATE | [do_loan_collateral_out](api.md#do-loan-collateral-out) |
| `KRD_SKOR_GIROV_OTHER_C` | SELECT / UPDATE | [do_loan_collateral_out](api.md#do-loan-collateral-out) |
| `KRD_TEKLIF` | SELECT | [init_global_variables](api.md#init-global-variables) |
| `KRD_TEKLIF_DETAY` | SELECT / UPDATE | [evaluate_limit_amount](api.md#evaluate-limit-amount), [reverse_update](api.md#reverse-update), [do_create_tranche](api.md#do-create-tranche), [get_gl_acc_from_matrix](api.md#get-gl-acc-from-matrix) and more |
| `KRD_TEKLIF_NO` | INSERT / UPDATE | [get_offer_id](api.md#get-offer-id) |
| `KRD_TEMINAT_TIP_PR` | SELECT | [do_loan_collateral_out](api.md#do-loan-collateral-out) |
| `KRD_TESIS` | SELECT / UPDATE | [create_account](api.md#create-account), [do_commission_recognition](api.md#do-commission-recognition), [do_guarantee_out](api.md#do-guarantee-out), [do_non_cash_loan_close](api.md#do-non-cash-loan-close) and more |
| `LOAN_ACCOUNTS` | SELECT | [create_account](api.md#create-account) |
| `LOAN_ACC_TYPES_PR` | SELECT | [post_int_amount_to_plan](api.md#post-int-amount-to-plan), [get_amount_for_pen_calc](api.md#get-amount-for-pen-calc-1), [create_account](api.md#create-account), [get_new_acc](api.md#get-new-acc) |
| `LOAN_ACC_TYPE_MAPPING` | SELECT | [get_acc_type_by_status](api.md#get-acc-type-by-status) |
| `LOAN_AMOUNT_RANGE_INFO` | SELECT | [get_amount_by_range](api.md#get-amount-by-range) |
| `LOAN_API.GET_GL_ACC_FROM_MATRIX` | SELECT | [create_account](api.md#create-account) |
| `LOAN_CATEGORY` | DELETE / INSERT / SELECT | [table_log_operation](api.md#table-log-operation) |
| `LOAN_CATEGORY_TEMP` | DELETE / INSERT / SELECT | [table_log_operation](api.md#table-log-operation) |
| `LOAN_EOD_AUTO_CLOSE` | INSERT / SELECT | [do_Loan_Close_With_Collateral_Out](api.md#do-loan-close-with-collateral-out) |
| `LOAN_EOD_CONTROL` | INSERT / SELECT | [do_loan_control](api.md#do-loan-control-1), [do_loan_control](api.md#do-loan-control-2) |
| `LOAN_EOD_CONTROL_EXP` | SELECT | [do_plan_control](api.md#do-plan-control), [do_loan_control](api.md#do-loan-control-2) |
| `LOAN_FLOW_RATIO_INFO` | DELETE / INSERT / SELECT | [table_log_operation](api.md#table-log-operation), [do_int_calculation](api.md#do-int-calculation), [get_flow_ratio_info](api.md#get-flow-ratio-info) |
| `LOAN_FLOW_RATIO_INFO_LOG` | INSERT / SELECT | [table_log_operation](api.md#table-log-operation) |
| `LOAN_GLOBAL_PARAMETERS_PR` | SELECT | [get_gl_value](api.md#get-gl-value) |
| `LOAN_HISTORY_MAPPING` | SELECT | [add_column_update](api.md#add-column-update-1) |
| `LOAN_INT_CALCULATION_DIFF_HISTORY` | DELETE / INSERT / SELECT / UPDATE | [loan_int_diff_operation](api.md#loan-int-diff-operation) |
| `LOAN_INT_CALC_STOP_FOR_GRACE` | SELECT | [do_int_calculation](api.md#do-int-calculation) |
| `LOAN_INT_CALC_TYPES_PR` | SELECT | [get_interest_calc_info](api.md#get-interest-calc-info), [get_basis_year_days_cnt](api.md#get-basis-year-days-cnt) |
| `LOAN_OPERATION_DESC` | SELECT | [get_trn_caller_id](api.md#get-trn-caller-id), [create_journal_entries](api.md#create-journal-entries), [create_loan_history](api.md#create-loan-history), [update_loan_history](api.md#update-loan-history) |
| `LOAN_OPERATION_HISTORY` | INSERT / MERGE / SELECT / UPDATE | [get_additional_info](api.md#get-additional-info), [reverse_update](api.md#reverse-update), [do_delete_operation](api.md#do-delete-operation), [do_loan_control](api.md#do-loan-control-2) and more |
| `LOAN_OPERATION_VOUCHER` | SELECT | [create_journal_entries](api.md#create-journal-entries) |
| `LOAN_OVERDUE_MAPPING` | SELECT | [do_overdue_transit_operation](api.md#do-overdue-transit-operation) |
| `LOAN_OVERDUE_TRANSIT_QUEUE` | SELECT | [do_overdue_transit_operation](api.md#do-overdue-transit-operation) |
| `LOAN_PAYMENT_PLAN` | DELETE / INSERT / SELECT / UPDATE | [post_int_amount_to_plan](api.md#post-int-amount-to-plan), [get_amount_for_pen_calc](api.md#get-amount-for-pen-calc-1), [get_ovd_trs_oper_type](api.md#get-ovd-trs-oper-type), [get_grace_info](api.md#get-grace-info) and more |
| `LOAN_PAYMENT_PLAN_LOG` | INSERT / SELECT | [table_log_operation](api.md#table-log-operation) |
| `LOAN_PORTFOLIO_LITE` | SELECT | [do_loan_status_control](api.md#do-loan-status-control), [do_Loan_Close_With_Collateral_Out](api.md#do-loan-close-with-collateral-out) |
| `LOAN_SPECIAL_DAYS_PR` | SELECT | [get_amount_for_pen_calc](api.md#get-amount-for-pen-calc-2) |
| `LOAN_STOP_RATIO_INFO` | DELETE / INSERT / SELECT | [table_log_operation](api.md#table-log-operation), [do_int_calculation](api.md#do-int-calculation), [get_stop_ratio_info](api.md#get-stop-ratio-info) |
| `LOAN_STOP_RATIO_INFO_LOG` | INSERT / SELECT | [table_log_operation](api.md#table-log-operation) |
| `LOAN_TEMPORARY_PAYMENT_PLAN` | INSERT / SELECT | [UPDATE_PAYMENT_PLAN](api.md#update-payment-plan) |
| `LOAN_TRANCHE_INFO` | SELECT | [add_column_update](api.md#add-column-update-1) |
| `LOAN_TRANCHE_LIMIT_CHANGES_HISTORY` | SELECT | [do_Loan_Close_With_Collateral_Out](api.md#do-loan-close-with-collateral-out) |
| `LOAN_TRANCHE_PAYMENT_PLAN` | SELECT / UPDATE | [post_int_amount_to_plan](api.md#post-int-amount-to-plan) |
| `ODEME_PLAN_TMP` | SELECT | [UPDATE_PAYMENT_PLAN](api.md#update-payment-plan) |
| `ODEME_PLAN_TMP2` | SELECT / UPDATE | [get_special_schedule](api.md#get-special-schedule) |
| `OPERATIONS.` | UPDATE | [add_additional_info](api.md#add-additional-info-1), [add_column_update](api.md#add-column-update-1), [table_log_operation](api.md#table-log-operation) |
| `PAYMENT` | UPDATE | [UPDATE_PAYMENT_PLAN](api.md#update-payment-plan) |
| `PKRD_TURKOD_PR` | SELECT | [get_overdue_min_amount](api.md#get-overdue-min-amount), [get_overdue_grace_days](api.md#get-overdue-grace-days) |
| `SP_FAIZ_GUN_TANIM_PR` | SELECT | [create_account](api.md#create-account) |
| `SP_URUN_PR` | SELECT | [get_gl_acc_from_matrix](api.md#get-gl-acc-from-matrix) |
| `SS_MUH1201_0_LOG` | SELECT | [do_journal_entry](api.md#do-journal-entry), [create_journal_entries](api.md#create-journal-entries) |
| `TEMP_CARD_BALANCE` | INSERT | [create_overdrafts](api.md#create-overdrafts) |

## Relationship evidence and material modifications

- Joins between loan master records, accounts, plans, and operation history in this package are **observed query relationships**, not verified foreign keys. No DDL establishing cardinality was supplied.
- Repayment-plan changes, loan account activity, history writes, and journal processing should be reviewed through the corresponding method entries.
- Objects touched inside called packages are external implementation dependencies, not direct reads/writes by `LOAN_API`.

