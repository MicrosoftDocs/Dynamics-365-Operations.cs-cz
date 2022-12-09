---
title: Problémy asynchronní synchronizace objednávek
description: Tento článek popisuje běžné důvody selhání asynchronního vytváření objednávky v Microsoft Dynamics 365 Commerce a poskytuje kroky k odstraňování problémů, které uživatelům systému a partnerům pomohou pochopit, co se stalo.
author: Shajain
ms.date: 11/30/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: 27bccced3c07149fe1842524660447a49f86f3fc
ms.sourcegitcommit: 2804b05214c87f76457608b5db072582ff339852
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/01/2022
ms.locfileid: "9815749"
---
# <a name="asynchronous-order-synchronization-issues"></a>Problémy asynchronní synchronizace objednávek

[!include [banner](../../includes/banner.md)]

Tento článek popisuje běžné důvody selhání asynchronního vytváření objednávky v Microsoft Dynamics 365 Commerce a poskytuje kroky k odstraňování problémů, které uživatelům systému a partnerům pomohou pochopit, co se stalo.

## <a name="symptom"></a>Příznak

Asynchronní objednávky vytvořené z elektronického obchodování nebo pokladního místa (POS) Dynamics 365 Commerce se v Commerce headquarters neprojevují.

## <a name="troubleshooting"></a>Řešení potíží

Vytvoření objednávky může selhat v headquarters z různých důvodů v závislosti na fázi, ve které proces vytváření objednávky selže. Následující kroky pro odstraňování problémů procházejí možnými hlavními příčinami.

### <a name="validate-that-the-transaction-related-to-the-asynchronous-order-has-reached-headquarters"></a>Ověřte, že transakce související s asynchronní objednávkou dosáhla headquarters

U objednávek elektronického obchodování přejděte v headquarters na **Maloobchod a komerce \> Dotazy a zprávy \> Transakce online obchodu**. Pokud máte číslo potvrzení objednávky, filtrujte transakce zadáním čísla potvrzení do pole **ID referenčního kanálu** . Pokud nemáte potvrzovací číslo, filtrujte transakce zadáním čísla zákaznického účtu.

U objednávek POS otevřete stránku **Transakce obchodu** a filtrujte záznamy podle čísla účtenky nebo čísla zákaznického účtu. Pokud transakce není nalezena, spusťte úlohu transakce kanálu **P-0001**, která synchronizuje transakce z kanálů do headquarters. Pokud úloha **P-0001** selže, otevřete lístek podpory pro selhání úlohy. Pokud je úloha **P-0001** úspěšná, ale transakce se stále nezobrazují v headquarters, otevřete lístek podpory, který obsahuje příslušné informace.
 
### <a name="check-the-synchronization-status-if-the-transaction-is-present-in-headquarters-but-isnt-linked-with-a-sales-order"></a>Kontrola stavu synchronizace, pokud je transakce přítomna v headquarters, ale není propojena s prodejní objednávkou

Pokud je transakce přítomna v headquarters, ale prodejní objednávka nebyla vytvořena, otevřete stránku **Transakce online obchodu** a vyberte pevnou záložku **Stav synchronizace**. Pokud se úloha **Synchronizovat objednávky** pokusila synchronizovat tuto transakci, v poli **Stav čekající objednávky** by měl být uveden stav **Úspěch** nebo **Neúspěch**. Pokud je stav **Úspěch**, musí být u této transakce přítomno pole prodejní objednávky. Pokud je stav **Chyba**, můžete si údaje o chybě zobrazit v poli **Podrobnosti o chybě objednávky** na záložce **Stav synchronizace**. Pokud není zobrazen žádný z těchto stavů, nebyl učiněn žádný pokus o zpracování transakce. V tomto případě můžete vybrat **Synchronizovat objednávku** v horní části stránky a spustit úlohu synchronizace.

Zajistěte, aby úloha **Synchronizace objednávek** byla naplánována na pravidelné spouštění, aby bylo možné vytvářet asynchronní transakce jako objednávky v headquarters.

Následující části poskytují informace o některých běžných chybách a jejich navrhovaných opravách.

#### <a name="the-order-error-details-field-shows-the-following-error-message-number-sequence-has-been-exceeded"></a>V poli Podrobnosti o chybě objednávky se zobrazuje následující chybová zpráva: „Posloupnost čísel byla překročena“

Číselné řady se používají k vytváření prodejních zakázek v headquarters. Pokud jsou vyčerpána všechna čísla povolená pro číselnou řadu, systém vygeneruje tuto chybovou zprávu. Číselnou řadu, která se používá k vytvoření prodejních objednávek, naleznete na **Parametry pohledávek \> Číselné řady \> Prodejní objednávka**. Chcete-li tuto chybu opravit, opravte stávající číselnou řadu nebo ji nahraďte novou číselnou řadou.

#### <a name="the-order-error-details-field-shows-the-following-error-message-there-must-be-a-default-payment-service-to-process-credit-card-transactions"></a>Podrobnosti chyby objednávky ukazují následující chybovou zprávu: „Ke zpracování transakcí kreditní kartou musí existovat výchozí platební služba“

Chcete-li tuto chybu opravit, potvrďte, že je v headquarters definována výchozí platba. Pokud není definována žádná výchozí platba, musíte ji definovat. Přejděte na **Pohledávky \> Nastavení plateb \> Platební služby** a ujistěte se, že je možnost **Výchozí zpracovatel pro nové kreditní karty** nastavena na **Ano** pro jednu platební službu.
    
#### <a name="the-order-error-details-field-shows-an-account-structure-error-message"></a>Pole Podrobnosti o chybě objednávky zobrazuje chybovou zprávu o struktuře účtu

Text chybové zprávy o struktuře účtu se může lišit, jak ukazují následující příklady. Chyby však sdílejí společnou hlavní příčinu, která souvisí s konfigurací struktury účtu.

- „Zaúčtování výsledků pro číslo šarže deníku 0009656328 doklad ARP-000959899 1,00 pro doklad ARP-000959899 ve společnosti usrt bude zaúčtován jako přeplatek nebo nedoplatek“
- „Zaúčtování výsledků pro číslo šarže deníku 0009656328 doklad ARP-000959899 doklad ARP-000959901 struktura účtu, pro kombinaci 618160, není platná pro hlavní účetní knihu sdílenou“
- „Zaúčtování výsledků pro číslo šarže deníku 0009656328 doklad ARP-000959899 doklad ARP-000959901 Hlášeno z firemních účtů usrt“
- „Zaúčtování výsledků pro číslo šarže deníku 0009656328 doklad ARP-000959899 zaúčtování bylo zrušeno“
    
Chcete-li tyto chyby opravit, zkontrolujte správnost struktur účtu. Další informace naleznete v tématu [Konfigurace struktur účtu](/dynamics365/finance/general-ledger/configure-account-structures).
    
Po opravě chyby vyberte neúspěšnou transakci a poté vyberte **Synchronizovat objednávku** v horní části stránky, abyste spustili úlohu synchronizace.
    
#### <a name="other-types-of-errors-that-might-require-the-transaction-data-to-be-fixed"></a>Jiné typy chyb, které mohou vyžadovat opravu dat transakce

Chcete-li opravit další typy chyb, které mohou vyžadovat opravu dat transakcí, můžete použít funkci „upravit a auditovat transakce“. Další informace viz [Úprava a audit transakcí](../edit-order-trans.md).
