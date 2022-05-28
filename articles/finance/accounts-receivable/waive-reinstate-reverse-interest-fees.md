---
title: Vzdát, obnovit nebo změnit úrokové poplatky
description: Tento článek popisuje, jak odpustit, obnovit a stornovat poplatky za úroky a jiné poplatky.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustInterestJourList
audience: Application User
ms.reviewer: kfend
ms.custom: 59461
ms.assetid: 25ec29f3-e3ea-4abb-bf6b-f6240873b315
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee37f7183758798de9d4dbe42fbff1662f742026
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724974"
---
# <a name="waive-reinstate-or-reverse-interest-fees"></a>Vzdát, obnovit nebo změnit úrokové poplatky

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak odpustit, obnovit a stornovat poplatky za úroky a jiné poplatky.

Můžete pomocí tlačítek na kartě **Sbírat** stránky se seznamem **všech zákazníků** vzdát, zrušit nebo obnovit poplatky:

-   Zrušené poplatky jsou odpuštěny. Můžete například v rámci dobrých obchodních vztahů odpustit poplatek odběrateli, který nesouhlasí s jeho zaplacením.
-   Obnovené poplatky se stanou znovu splatnými. Můžete znovu nárokovat poplatky, které byly dříve odpuštěny. Možná budete muset znovu nárokovat poplatek, pokud zjistíte, že neměla být vzdán.
-   Stornované poplatky jsou odebrány z účtu zákazníka a nejsou nadále splatné. Můžete například stornovat poplatek, pokud byla vybrána nesprávná úroková míra k výpočtu částky, kterou má odběratel zaplatit. Můžete použít samostatný proces pro opětovný výpočet a tvorbu oznámení úroků, který obsahuje nové platby pro odběratele.

Všechny tyto akce mění oznámení úroků. Oznámení úroků, které je obchodním dokladem informujícím odběratele o stržení poplatků z jejich účtu. Když odpustíte nebo stornujete úrok nebo poplatky, dobropisu nebo vyrovnávací faktura je automaticky vytvořena k vyrovnání nákladů. Pokud obnovíte odpuštěné poplatky, je automaticky vytvořena faktury s částkou MD pro obnovení poplatku, který odběratel dluží. Následující tabulky popisují výsledek každé akce.

| Akce                                                                                                                                                                                                            | Výsledek pro odběratele                                                                                             | Proces                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Úplné odpuštění všech oznámení úroků se všemi úroky a poplatky, které zahrnují. –nebo– Výběr a odpuštění poplatků a úrokových transakcí, které jsou součástí oznámení úroků.                                        | Poplatky jsou odpuštěny.                                                                                           | Pro zákazníka je vytvořena faktura úprav nebo dobropis. Dobropis neslouží k automatickému vyrovnání oznámení úroků nebo transakcí úroků nebo poplatků, které jste vybrali. Vyrovnaná částka se rovná celkové výší poplatků, po odečtení všech předchozích plateb odběratele a po odečtení všech částek, které byly odpuštěny nebo odepsány. Pokud částka dobropisu přesahuje dlužnou částku odběratele, můžete převést dobropis k faktuře dodavatele. Pak můžete udělit zákazníkovi refundaci.                                                       |
| Úplné obnovení všech oznámení úroků se všemi úroky a poplatky, které zahrnují. –nebo– Výběr a opětovné nárokování poplatků a úrokových transakcí, které jsou součástí oznámení úroků.                                | Odpuštěná částka je znovu splatná.                                                                                     | Vytvoří se faktura s debetní částkou a částka je automaticky vyrovnána proti poplatkům, které byly dříve odpuštěny. Skutečná oznámení úroků nejsou znovu uplatněna. Místo toho je vytvořena faktura zobrazující částku, která je splatná od zákazníka. Dobropisy nebo úpravy faktur, které byly vytvořeny k vyrovnání odpuštěných oznámení úroků mohou stále existovat v případě, že nebyly použity k vyrovnání oznámení úroků. V takovém případě budou stornovány zbývající dobropisy. Zbývající dobropisy se obvykle automaticky vyrovnávají při odpuštění oznámení úroků. Zbývající dobropis však může existovat, pokud zákazník zaplatil za oznámení úroků i v případě, že zákazník rozporoval poplatky. |
| Stornovat veškeré oznámení úroků. –nebo– Storno vybraných úrokových transakcí, které jsou součástí oznámení úroků. **Poznámka:** Nemůžete stornovat poplatek. Můžete však stornovat celé oznámení úroků obsahující poplatek. | Poplatky od odběratele nejsou nadále splatné. Poplatky ovšem jsou znovu splatné v případě, že přepočítáte úrok. | Proces je stejný jako proces u odvolání oznámení úroků a vybraných úrokových transakcí. Pro zákazníka je vytvořena faktura úprav nebo dobropis. Tento dobropis se používá pro automatické vyrovnání oznámení úroků. Můžete použít samostatný proces pro přepočítání úroků a vytvoření nových oznámení úroků.                                                                                                                                                                                                                                                                                                                                                                                              |

> [!NOTE] 
> K odpisu nedobytných pohledávek můžete také použít samostatný proces. Tento proces označí všechny transakce odběratele pro vyrovnání, namísto upuštění od poplatků, které jsou součástí oznámení úroků.

## <a name="adjust-interest-for-invoices"></a>Úprava úroků pro faktury
Kromě úpravy oznámení úroků lze odebrat úrokové náklady na faktury pomocí jednoho z následujících postupů. Oba procesy také provedou úpravy v souvisejících oznámeních úroků.

### <a name="correct-an-invoice-that-has-associated-interest"></a>Oprava faktury s přidruženým úrokem

Můžete opravit zaúčtovanou fakturu, která je součástí oznámení úroků. Tento proces zkopíruje podrobnosti z existující faktury do nové faktury, aby byly provedeny pouze opravy, které chcete. Faktura je zrušena a je vytvořena nová faktura. Úrok z transakce je také stornován v oznámení úroků, pokud bylo oznámení úroků zaúčtováno. 

Opravy můžete provádět pomocí tlačítka **Správná faktura** v podokně akcí textu volné faktury. Toto tlačítko je k dispozici pouze, je-li vybrán konfigurační klíč **Oprava volné faktury**.

### <a name="reverse-a-customer-transaction-that-has-associated-interest"></a>Stornování transakce odběratele s přidruženým úrokem

Můžete použít ke stornování transakce odběratele na faktuře, pokud byla faktura vytvořena nesprávně. Pokud stornovaná transakce má úrok zahrnutý v oznámení úroků a oznámení úroků bylo zaúčtováno, úrok v transakci bude stornován v oznámení úroků. Oznámení úroků je zrušeno, pokud nebylo zaúčtováno. 

Transakce odběratele můžete stornovat použitím tlačítka **Zpět** na stránce **Transakce odběratele**.

## <a name="waive-or-reinstate-interest-notes"></a>Odpuštění nebo opětovné nárokování oznámení úroků
Můžete vzdát nebo znovu nárokovat všechny náklady na oznámení úroků, které vyberete. Když odpouštíte náklady, nesmí překročit celková odpuštěná částka žádný nastavený limit částek. Oznámení úroků lze obnovit pouze v případě, že dříve bylo odpuštěno. 

Lze odpustit nebo obnovit oznámení úroků použitím tlačítka **Oznámení úroků** na kartě **Shromáždit** na stránce **Odběratel**.

## <a name="waive-or-reinstate-interest-transactions"></a>Odpuštění nebo opětovné nárokování úrokových transakcí
Můžete odpustit nebo znovu nárokovat úrokové transakce pro oznámení úroků místo úpravy všech nákladů na oznámení úroků. Když odpouštíte náklady, nesmí překročit celková odpuštěná částka žádný nastavený limit částek. Můžete znovu nárokovat úrokové transakce pouze v případě, že byly dříve odpuštěny. 

Lze odpustit nebo obnovit oznámení úroků použitím tlačítka **Úrok z transakce** na kartě **Shromáždit** na stránce **Odběratel**.

## <a name="waive-or-reinstate-fees"></a>Odpuštění nebo opětovné nárokování poplatků
Můžete odpustit nebo znovu nárokovat poplatky pro oznámení úroků místo úpravy všech nákladů na oznámení úroků. Když odpouštíte náklady, nesmí překročit celková odpuštěná částka žádný nastavený limit částek. Poplatek lze obnovit, pouze v případě, že dříve byl odpuštěn. 

Lze odpustit nebo obnovit oznámení úroků použitím tlačítka **Poplatek** na kartě **Shromáždit** na stránce **Odběratel**.

## <a name="reverse-interest-notes"></a>Stornovat oznámení úroků
Můžete stornovat všechny náklady na oznámení úroků, které vyberete. Stornované poplatky jsou odebrány z účtu zákazníka a nejsou nadále splatné. Po stornování oznámení úroků, můžete přepočítat úroky a vytvořit nové oznámení úroků. 

Lze stornovat oznámení úroků použitím tlačítka **Oznámení úroků** na kartě **Shromáždit** na stránce **Odběratel**.

## <a name="reverse-interest-transactions"></a>Stornování úrokových transakcí
Je možné stornovat všechny úrokové transakce, které vyberete. Stornované poplatky jsou odebrány z účtu zákazníka a nejsou nadále splatné. Po stornování transakcí můžete přepočítat úrok a vytvořit nové oznámení úroků.

Lze stornovat úroky z transakce použitím tlačítka **Úrok z transakce** na kartě **Shromáždit** na stránce **Odběratel**.

## <a name="view-the-history-of-adjustments-for-charges-that-were-waived-reinstated-or-reversed"></a>Zobrazení historie úprav pro náklady, které byly odpuštěny, obnoveny nebo stornovány
Můžete zobrazit podrobnou historii úprav, která byly provedena pro oznámení úroků, například uživatele, který zadal úpravu, typ úpravy, částku a kdy byla úprava zadána. Můžete například zobrazit předchozí úpravy, které byly zadány pro oznámení úroků před tvorbou nového oznámení úroků. 

Lze stornovat úroky z transakce použitím tlačítka **Historie** na kartě **Shromáždit** na stránce **Odběratel**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
