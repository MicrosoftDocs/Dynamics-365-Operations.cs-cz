---
title: "Maloobchodní čas a docházka"
description: "Toto téma popisuje scénáře, které jsou podporovány pro správu času a docházky v Microsoft Dynamics 365 pro Provoz - Maloobchod."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 021f0ce8ee73ede482b2b74fce93f61a886288fc
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="retail-time-and-attendance"></a>Maloobchodní čas a docházka

[!include[banner](includes/banner.md)]


Toto téma popisuje scénáře, které jsou podporovány pro správu času a docházky v Microsoft Dynamics 365 pro Provoz - Maloobchod. 

<a name="manage-worker-setup-and-scheduling"></a>Spravovat nastavení pracovníka a plánování
----------------------------------

### <a name="initial-configuration"></a>Počáteční konfigurace 

-   Spusťte průvodce konfigurací.
-   Zaregistrujte pracovníky jako pracovníky s registrací času.

### <a name="plan-worker-schedules"></a>Plánování kalendářů pracovníka

-   Použijte profily pomocí plánovače práce. Další informace naleznete v tématu <https://technet.microsoft.com/en-us/library/aa551234.aspx>.

Informace o postupu konfigurace naleznete v tématu <https://technet.microsoft.com/en-us/library/aa496971.aspx>.

### <a name="retail-specific-configuration"></a>Maloobchodní plánovač – Konfigurace

-   Povolte funkční profil pro čas odchodu pro pracovníky, kterým chcete umožnit časovou registraci. Klikněte na tlačítko **Funkční profily POS** &gt; **Funkce** &gt; **Registrace času POS** &gt; **Povolit registrace času**.
-   Konfigurujte skupiny oprávnění pro pokladní místa (POS) a umožněte tak zobrazit oprávnění časových položek. Toto oprávnění umožňuje uživateli zobrazit časové záznamy jiných zaměstnanců v obchodě (a z jiných přidružených obchodů, ke kterým je uživatel přidružen, prostřednictvím adresáře). Je vhodné povolit toto oprávnění pro roli správce, ale ne pro roli pokladníka. Klikněte na tlačítko **Skupiny oprávnění POS** &gt; **Zobrazit záznamy časomíry**.

## <a name="register-time"></a>Čas pokladny
### <a name="cashier-and-non-cashier-time-registrations"></a>Čas registrace pokladníka / nepokladníka

-   V POS:
    -   Operace příchodu:
        -   Přihlaste se pomocí operace bez zásuvky nebo nové směny.
        -   Vyberte hodiny operace.
        -   Vyberte požadovanou operaci:
            -   Označení příchodu
            -   Přestávka v práci
            -   Přestávka na oběd
            -   Označení odchodu

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Aktuální stav</th>
    <th>Dostupné operace</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Označení příchodu</td>
    <td><ul>
    <li>Přestávka v práci</li>
    <li>Přestávka na oběd</li>
    <li>Označení odchodu</li>
    </ul></td>
    </tr>
    <tr class="even">
    <td>Přestávka v práci</td>
    <td>Označení příchodu</td>
    </tr>
    <tr class="odd">
    <td>Přestávka na oběd</td>
    <td>Označení příchodu</td>
    </tr>
    <tr class="even">
    <td>Označení odchodu</td>
    <td>Označení příchodu</td>
    </tr>
    </tbody>
    </table>

    [![StavyČasomíry](./media/timeclockstates.png)](./media/timeclockstates.png)
-   Prohlédněte si zprávu s ověřením a ověřte správnost času aktuální aktivity.
-   Protokolový deník:
    -   Klepnutím na tlačítko **Protokolový deník** zobrazíte časové aktivity.
    -   Časové filtry slouží k výběru různých časových oken.
    -   Při práci na více místech obchodu se zobrazí vaše registrace času ze všech obchodů, kde máte zaznamenaný čas. Filtr obchodu slouží k zobrazení času registrací z vybraného obchodu.

<!-- -->

-   Různá časová pásma:
    -   Při zobrazení času z jiného místa (pro pokladní deníky nebo pomocí **Zobrazit časové záznamy** pro scénáře správce), kdy se toto umístění nachází v jiném časovém pásmu, jsou zobrazené časové záznamy převedeny na místní časové pásmo. Například jste vedoucím dvou obchodů, jednoho v Arizoně a druhého v Nevadě. Pokladník zaregistruje příchod v 9:00 v Arizoně. V daném okamžiku je čas v Nevadě 8:00. Proto pokud jste v obchodě v Nevadě a podíváte se na záznamy registrace času, registrace času je označena jako 8:00.

## <a name="view-worker-time-registrations"></a>Zobrazit registrace pracovní doby pracovníků
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>Zobrazení registrací času pracovníka a filtrování podle typu obchodu nebo aktivity

V POS:

-   Vyberte **Zobrazit časové záznamy**.
-   Zobrazí se aktivity časové registrace od všech zaměstnanců přiřazených do stejných obchodů, ke kterým jste přiřazeni vy.
-   Můžete použít typ aktivity a uložit filtry pro filtrování registrace pracovní doby.

## <a name="process-and-manage-time-registrations"></a>Zpracovávat a spravovat registrace pracovní doby
Uživatel aplikace Dynamics 365 pro operace - maloobchod používá workflow pro výpočet, schvalování a převádění registrací pracovní doby do mzdového systému.

### <a name="primary-operations"></a>Primární operace

-   Vypočítat
-   Schválit
-   Odeslání pro mzdu

### <a name="other-common-operations"></a>Jiné běžné operace

-   Hromadný odchod
-   Registrování absence

Další informace o postupu zpracování času a docházky naleznete v tématu <https://technet.microsoft.com/en-us/library/aa573180.aspx>.




