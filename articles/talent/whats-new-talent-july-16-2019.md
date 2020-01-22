---
title: Co je nového nebo co se změnilo v aplikaci Dynamics 365 Talent (16. července 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 07/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-07-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6dce39bc529bf6dd6079ed900af12510c0773f9a
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899075"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-16-2019"></a>Co je nového nebo co se změnilo v aplikaci Dynamics 365 Talent (16. července 2019)

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract
Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Attract.

### <a name="coming-soon-in-attract"></a>Již brzy v aplikaci Attract
#### <a name="job-approvals-appear-on-the-home-page"></a>Schválení práce se zobrazí na domovské stránce

Schválení se zobrazují v části **Schválení** na řídicím panelu. Schvalovatelé mohou zkontrolovat svá schválení v části **Přiřazeno vám**, která zobrazuje ID práce, pracovní pozici, ostatní schvalovatele a datum přiřazení práce. Uživatelé, kteří odesílají práci ke schválení, mohou revidovat své práce v části **Vyžádáno vámi**, která zobrazuje schvalovatele, kteří musí schválit odeslanou práci.

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard
Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Změny v Core HR
Změny popsané v této části se vztahují na číslo sestavení 8.1.2390.

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>Entity Common Data Service, které nyní podporují vlastní pole

- BusinessProcessCalendar                     
- BusinessProcessGroupAssignment         
- BusinessProcessStage                          
- BusinessProcessTemplateHeader          
- BusinessProcessTemplateTask            
- HcmBenefitOption                              
- HcmBenefitType                                  
- HcmCompensationGrid                            
- HcmCompensationLevel                          
- HcmCompensationPayFrequency                 
- HcmCompensationReferencePointSetup        
- HcmCompensationReferencePointSetupLine 
- HcmCompensationRegion                     
- HcmCompFixedPlanTable                     
- HcmEmployment                                
- HcmEthnicOrigin                                
- HcmFixedCompensationEvent                 
- HcmJob                                           
- HcmJobFunction
- HcmJobType
- HcmLanguageCode
- HcmPayrollCalculationFrequency
- HcmPosition
- HcmPositionType
- HcmSkillType
- HcmVeteranStatus
- HcmWorkCalendarHoliday
- HcmWorkCalendarHolidayLine
- HcmWorker
- HcmWorkerPersonalDetail
- LeaveType
- OMDepartment
- OMLegalEntity
- PayCycle
- PayPeriod
- PayrollBenefitCalculationRate
- PayrollBenefitCalculationRateDetail
- PayrollEarningCode

### <a name="unable-to-see-goals-and-reviews-in-manager-self-service"></a>Nelze zobrazit cíle a recenze na samoobslužné stránce manažera.

Změny z tohoto týdne umožňují zobrazit a upravit cíle a recenze pro manažery na úrovni přeskakování v samoobslužných stránkách manažera.

### <a name="goal-form-cannot-be-closed-after-a-user-edits-any-goal-field"></a>Formulář cíle nelze zavřít, poté, co uživatel upraví některé z polí cíle

Tato verze opravuje problémy, kdy se při výběru tlačítka **Zavřít** nezavře formulář cíle.

### <a name="creating-new-goals-and-saving-displays-error"></a>Vytvoření nových cílů a ukládání zobrazí chybu

Tato verze opravuje problém při ukládání cílů do samoobslužné služby pro zaměstnance a manažera.

### <a name="unable-to-add-a-field-to-position-details"></a>Nelze přidat pole k podrobnostem pozice. 

V této verzi jsou nyní podporována vlastní pole s podrobnostmi pozice.
 
### <a name="unable-to-set-up-expiring-date-on-the-earning-code-through-data-management"></a>Nelze nastavit datum vypršení platnosti v kódu pro získávání prostřednictvím správy dat

Změny nyní umožňují nastavit data vypršení platnosti pro kódy příjmů ve správě dat.

### <a name="new-custom-fields-dont-sync-quickly-enough"></a>Nová vlastní pole nejsou dostatečně rychle synchronizována.

Výkonnost vlastní synchronizace pole do Common Data Service byla vylepšena ve vydání z tohoto týdne.

### <a name="entity-export-to-database-jobs-fail-with-error-message-format-of-the-initialization-string-does-not-conform-to-specification-starting-at-index-0"></a>Export entity do databázových úloh selhává s chyborou zprávou: "Formát inicializačního řetězce neodpovídá specifikaci začínající v indexu 0."

Toto vydání opravuje problém, kdy selhávají úlohy dávkového zpracování databáze. Ruční aktualizace:

1. Přejděte do části **Správa dat**.
2. Vyberte **Konfigurovat export entit do databáze**.
3. Znovu zadejte připojovací řetězec do cílové databáze a vyberte možnost **Uložit**.

### <a name="smtp-email-configuration-suddenly-fails-with-error-message-the-smtp-server-requires-a-secure-connection-or-the-client-was-not-authenticated"></a>E-mailová konfigurace protokolu SMTP se náhle nezaří s chybovou zprávou: "Server SMTP vyžaduje zabezpečené připojení nebo klient nebyl ověřen."

Tato verze opravuje e-mailovou konfiguraci protokolu SMTP, která náhle selhala. Ruční aktualizace:

1. Přejděte na **Správa systému**.
2. Vyberte **Parametry e-mailu**.
3. Vyberte **Nastavení SMTP**. 
4. Zadejte znovu uživatelské jméno a heslo používané pro server SMTP a vyberte tlačítko **Uložit**.

## <a name="in-preview"></a>Náhled

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Funkce Preview jsou povoleny pouze v instancích sandbox.

Když zřizujete novou instanci aplikace Talent, můžete určit, zda je typem instance **Produkce** nebo **Sandbox**. Instance typu **Sandbox** umožňují dřívější testování nových funkcí. Všechny existující instance aplikace Talent budou aktualizovány na typ instance **Produkční**. Chcete-li, aby byla jedna z existujících instancí aktualizována na typ instance **Sandbox**, obraťte se na [podporu](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) a inicializujte požadavek na změnu.

Další informace o tom, jak jsou publikovány změny, naleznete v části [Zřízení aplikace Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Omezení typů pracovního volna v žádostech o volno

Organizace mohou nabízet mnoho různých typů volna svým zaměstnancům. Pro zaměstnance však nemusí být vhodné odesílat požadavky na volno u některých typů pracovního volna. Tyto typy pracovního volna mohou být namísto toho spravovány oddělením HR. V této verzi můžete konfigurovat, pro které typy pracovního volna mohou zaměstnanci odesílat žádosti o volno. 

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>Zobrazení informací o výkonu pro přímé a rozšířené podřízené v samoobsluze pro manažery

Nová možnost umožní, aby manažeři zobrazili výkon svých přímých podřízených i jejich rozšířených podřízených. V současné době mohou linioví manažeři přiřazovat a aktualizovat cíle výkonnosti a vydávat nové revize. Kromě toho mohou přímí manažeři a jejich zaměstnanci udržovat a aktualizovat deníky výkonnosti, aby byl zajištěn plynulý proces kontroly výkonu. Při implementaci této změny budou mít manažeři možnost zobrazit a udržovat informace související s výkonem pro své rozšířené podřízené spolu se svými přímými podřízenými.
