---
title: "Správa času a docházky v aplikaci Retail"
description: "Toto téma popisuje scénáře, které jsou podporovány pro správu času a docházky v Microsoft Dynamics 365 for Retail."
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 4c54909a02376a62a72a986e634649fa0ae54284
ms.contentlocale: cs-cz
ms.lasthandoff: 01/04/2019

---

# <a name="time-and-attendance-management-in-retail"></a>Správa času a docházky v aplikaci Retail

[!include [banner](includes/banner.md)]

Toto téma popisuje scénáře, které jsou podporovány pro správu času a docházky v Microsoft Dynamics 365 for Retail.

## <a name="manage-worker-setup-and-scheduling"></a>Spravovat nastavení pracovníka a plánování

### <a name="initial-configuration"></a>Počáteční konfigurace 

- Spusťte průvodce konfigurací.
- Zaregistrujte pracovníky jako pracovníky s registrací času.

### <a name="plan-worker-schedules"></a>Plánování kalendářů pracovníka

- Použijte profily pomocí plánovače práce. Další informace viz [Použijte profily žádostí pomocí plánovače práce](https://technet.microsoft.com/library/aa551234.aspx).

Informace o konfiguraci naleznete v tématu [Nastavení modulu čas a docházka](https://technet.microsoft.com/library/aa496971.aspx).

### <a name="retail-specific-configuration"></a>Maloobchodní plánovač – Konfigurace

- Povolte funkční profil pro čas odchodu pro pracovníky, kterým chcete umožnit časovou registraci. Klikněte na tlačítko **Funkční profily POS** &gt; **Funkce** &gt; **Registrace času POS** &gt; **Povolit registrace času**.
- Konfigurujte skupiny oprávnění pro pokladní místa (POS) a umožněte tak zobrazit oprávnění časových položek. Toto oprávnění umožňuje uživateli zobrazit časové záznamy jiných zaměstnanců v obchodě (a z jiných přidružených obchodů, ke kterým je uživatel přidružen, prostřednictvím adresáře). Je vhodné povolit toto oprávnění pro roli správce, ale ne pro roli pokladníka. Klikněte na tlačítko **Skupiny oprávnění POS** &gt; **Zobrazit záznamy časomíry**.

## <a name="register-time"></a>Čas pokladny

### <a name="cashier-and-non-cashier-time-registrations"></a>Čas registrace pokladníka / nepokladníka

- V POS:

    - Operace příchodu:

        - Přihlaste se pomocí operace bez zásuvky nebo nové směny.
        - Vyberte hodiny operace.
        - Vyberte požadovanou operaci:

            - Označení příchodu
            - Přestávka v práci
            - Přestávka na oběd
            - Označení odchodu

        <table>
        <thead>
        <tr>
        <th>Aktuální stav</th>
        <th>Dostupné operace</th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td>Označení příchodu</td>
        <td>
        <ul>
        <li>Přestávka v práci</li>
        <li>Přestávka na oběd</li>
        <li>Označení odchodu</li>
        </ul>
        </td>
        </tr>
        <tr>
        <td>Přestávka v práci</td>
        <td>Označení příchodu</td>
        </tr>
        <tr>
        <td>Přestávka na oběd</td>
        <td>Označení příchodu</td>
        </tr>
        <tr>
        <td>Označení odchodu</td>
        <td>Označení příchodu</td>
        </tr>
        </tbody>
        </table>

        [![StavyČasomíry](./media/timeclockstates.png)](./media/timeclockstates.png)

- Prohlédněte si zprávu s ověřením a ověřte správnost času aktuální aktivity.
- Protokolový deník:

    - Klepnutím na tlačítko **Protokolový deník** zobrazíte časové aktivity.
    - Časové filtry slouží k výběru různých časových oken.
    - Při práci na více místech obchodu se zobrazí vaše registrace času ze všech obchodů, kde máte zaznamenaný čas. Filtr obchodu slouží k zobrazení času registrací z vybraného obchodu.

- Různá časová pásma:

    - Při zobrazení času z jiného místa (pro pokladní deníky nebo pomocí **Zobrazit časové záznamy** pro scénáře správce), kdy se toto umístění nachází v jiném časovém pásmu, jsou zobrazené časové záznamy převedeny na místní časové pásmo. Například jste vedoucím dvou obchodů, jednoho v Arizoně a druhého v Nevadě. Pokladník zaregistruje příchod v 9:00 v Arizoně. V daném okamžiku je čas v Nevadě 8:00. Proto pokud jste v obchodě v Nevadě a podíváte se na záznamy registrace času, registrace času je označena jako 8:00.

## <a name="view-worker-time-registrations"></a>Zobrazit registrace pracovní doby pracovníků

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>Zobrazení registrací času pracovníka a filtrování podle typu obchodu nebo aktivity

V POS:

- Vyberte **Zobrazit časové záznamy**.
- Zobrazí se aktivity časové registrace od všech zaměstnanců přiřazených do stejných obchodů, ke kterým jste přiřazeni vy.
- Můžete použít typ aktivity a uložit filtry pro filtrování registrace pracovní doby.

## <a name="process-and-manage-time-registrations"></a>Zpracovávat a spravovat registrace pracovní doby

Uživatel aplikace Dynamics 365 for Retail používá workflow pro výpočet, schvalování a převádění registrací pracovní doby do mzdového systému.

### <a name="primary-operations"></a>Primární operace

- Vypočítat
- Schválit
- Odeslání pro mzdu

### <a name="other-common-operations"></a>Jiné běžné operace

- Hromadný odchod
- Registrování absence

Další informace o zpracování registrace času a docházky naleznete v tématu [Zpracování registrací času a docházky](https://technet.microsoft.com/library/aa573180.aspx).

