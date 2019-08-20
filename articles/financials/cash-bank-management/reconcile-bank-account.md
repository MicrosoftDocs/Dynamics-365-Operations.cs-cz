---
title: Odsouhlasení bankovního účtu
description: Toto téma popisuje způsob odsouhlasení bankovního účtu.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e9a9d1c53a4b9e764c1592cca898cd6f3293594
ms.sourcegitcommit: 299e20b59ebefa584ed46a13da3f1a7ff709e43c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2019
ms.locfileid: "1863625"
---
# <a name="reconcile-a-bank-account"></a>Odsouhlasení bankovního účtu

[!include[banner](../includes/banner.md)]

Když obdržíte bankovní výpis, měli byste pravidelně odsouhlasit bankovní transakce právnických osob s transakcemi na bankovním výpisu.

V případě, že se některá z plateb šeků nebo vkladových složenek uvedených na výpisu nachází ve stavu **Čekající zrušení**, nemůžete výpis z bankovního účtu odsouhlasit. Pokud kontrolor zaúčtuje nebo zamítne stornování šeku nebo zrušení platby vkladové složenky, platby se již nenachází ve stavu **Čekající zrušení** a bankovní účet je možné odsouhlasit.

1.  Přejděte na **Pokladna a banka** \> **Bankovní účty** \> **Bankovní účty**. Vyberte bankovní účet, který chcete odsouhlasit s bankovním výpisem, a vyberte **Odsouhlasit** > **Odsouhlasení účtu**.

2.  Zadejte informace do polí **Datum bankovního výpisu** a **Bankovní výpis**. Do pole **Konečný zůstatek** můžete zadat zůstatek bankovního účtu, jak je zobrazen ve výpisu z bankovního účtu.

3.  Výběrem možnosti **Transakce** otevřete stránku **Odsouhlasení účtu**.

4.  Pro každou transakci zahrnutou na výpisu z bankovního účtu zaškrtněte pole **Proplaceno**, pokud částka v aplikaci Microsoft Dynamics 365 for Finance and Operations odpovídá částce na výpisu z bankovního účtu. Můžete také zadat nebo změnit hodnotu v poli **Typ bankovní transakce**. Toto pole je důležité pro statistiky bankovních transakcí a některé zprávy.
    

    > [!NOTE]
    > <P>Políčko <STRONG>Proplaceno</STRONG> nezaškrtávejte pro transakce, které se nenachází na výpisu z bankovního účtu. Tyto transakce se budou zobrazovat na této stránce, dokud nebudou odsouhlaseny s budoucím výpisem z bankovního účtu.</P>
    > <P>V případě, že se transakce nachází ve stavu <STRONG>Čekající zrušen</STRONG>, zaškrtávací políčko <STRONG>Proplaceno</STRONG> není k dispozici. Transakce se v tomto stavu mohou nacházet v případě, že nastavení aplikace Finance and Operations vyžaduje odeslání stornování nebo zrušení ke kontrole před zaúčtováním. Poté, co kontrolor zaúčtuje nebo zamítne stornování nebo zrušení, platby se již nenachází ve stavu <STRONG>Čekající zrušení</STRONG> a bankovní účet je možné odsouhlasit s bankovním výpisem.</P>

    
    Chcete-li zaškrtnout políčko **Proplaceno** u intervalu šeků, které jsou všechny zobrazeny v bankovním výpisu, vyberte **Označit interval šeků** a potom určete interval.

5.  Pokud částka pro transakci bankovního účtu neodpovídá částce transakce v bankovním výpisu, zadejte částku opravy do pole **Částka opravy**.
    

    > [!NOTE]
    > <P>Pokud je fiskální období transakce, která má být opravena, uzavřeno, nelze pole <STRONG>Částka opravy</STRONG> použít. Místo toho je nutné vytvořit řádek s datem transakce v otevřeném fiskálním období opravy. V tomto případě je nutné přidat finanční dimenze použité v původní transakci a také hlavní protiúčet.</P>



6.  Vytvořte transakce pro položky, jako jsou například poplatky úroky, které jsou uvedeny na výpisu z bankovního účtu, ale nejsou zaznamenány v aplikaci Finance and Operations. Zadejte **Typ bankovní transakce** a příslušné finanční dimenze.

7.  Pokud jsou transakce na výpisu z bankovního účtu označeny jako **Proplacené**, částka v poli **Neodsouhlaseno**, která je při provádění změn průběžně přepočítávána, se blíží nule. Jakmile dosáhne nuly, můžete kliknutím na tlačítko **Odsouhlasit účet** zaúčtovat odsouhlasení a transakce a opravy, které jste vytvořili.
    
    Po zaúčtování odsouhlasení již nelze dále kontrolovat a upravovat zahrnuté transakce a tyto transakce se v budoucím odsouhlasení účtu již nezobrazí.

8.  Chcete-li zobrazit bankovní transakce, které ještě nebyly odsouhlaseny, použijte sestavu **Neodsouhlasené bankovní transakce**. Chcete-li zobrazit bankovní výpis bankovního účtu, použijte sestavu **Bankovní výpis.**

# <a name="cancel-bank-statement-reconciliation"></a>Zrušení odsouhlasení bankovního výpisu 

Funkce Zrušení odsouhlasení bankovního výpisu vám umožňuje zrušit odsouhlasení bankovního výpisu. Chcete-li použít tuto funkci, povolte funkci **Zrušení odsouhlasení bankovního výpisu** v pracovním prostoru **Správa funkcí**. Je také nutné povolit parametr **Povolit úpravy bankovního výpisu**. Chcete-li to udělat, přejděte na **Pokladna a banka > Nastavení > Parametry pokladny a banky > Odsouhlasení banky**.
 
Odsouhlasení bankovního výpisu lze zrušit pouze v chronologickém pořadí, ve kterém byly zadány. Když je odsouhlasení bankovního výpisu zrušeno, nové transakce a opravy budou stornovány a všechny ostatní transakce budou označeny jako Neodsouhlasené.
 
Chcete-li zrušit odsouhlasení bankovního výpisu, vyberte bankovní výpis a vyberte **Bankovní výpis > Zrušení odsouhlasení banky**. Na stránce **Storno odsouhlasení banky** zadejte **Kód důvodu**, **Komentář k důvodu** a **Datum zrušení**. Výběrem tlačítka **OK** zahajte zrušení. Poznámka: datum zrušení bankovního výpisu musí být v nebo po datu výpisu z banky. Po zrušení odsouhlasení bankovního výpisu bude pole **Datum zrušení** bankovního výpisu aktualizováno dle **Data zrušení**. Chcete-li zobrazit transakce, pro které bylo odsouhlasení zrušeno, vyberte tlačítko **Transakce**.
