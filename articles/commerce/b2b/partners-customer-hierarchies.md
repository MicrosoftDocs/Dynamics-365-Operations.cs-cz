---
title: Správa B2B obchodních partnerů pomocí zákaznických hierarchií
description: Tento článek popisuje, jak používat hierarchie zákazníků ke správě obchodních partnerů pro weby elektronického obchodování Microsoft Dynamics 365 Commerce typu business-to-business (B2B).
author: josaw1
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ddd02045b5df3ce20160a4feaa23339475823d3d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864974"
---
# <a name="manage-b2b-business-partners-using-customer-hierarchies"></a>Správa B2B obchodních partnerů pomocí zákaznických hierarchií

[!include [banner](../../includes/banner.md)]

Tento článek popisuje, jak používat hierarchie zákazníků ke správě obchodních partnerů pro weby elektronického obchodování Microsoft Dynamics 365 Commerce typu business-to-business (B2B).

V centrále Commerce se entita *hierarchie zákazníků* používá k reprezentaci organizací obchodních partnerů, které budou používat váš web elektronického obchodu B2B. Než začnete používat hierarchie zákazníků ke správě obchodních partnerů, musíte povolit možnosti elektronického obchodování B2B v centrále Commerce a poté definovat číselnou řadu pro hierarchii zákazníků.

## <a name="enable-the-b2b-e-commerce-feature-in-commerce-headquarters"></a>Zapnutí funkce B2B elektronického obchodování v centrále Commerce

Chcete-li používat možnosti elektronického obchodování B2B, musíte nejprve povolit funkci **Povolit využití funkcí B2B eCommerce** v centrále Commerce.

1. Přejděte na **Pracovní prostory \> Správa funkcí**.
1. Na kartě **Vše** vyhledejte pomocí pole filtru **Modul: Maloobchod a obchod**.
1. Najděte funkci **Povolit využití funkcí B2B eCommerce**, vyberte ji, a potom vyberte v pravém dolním rohu příkaz **Povolit nyní**.

## <a name="define-a-number-sequence-for-the-customer-hierarchy"></a>Definování číselné řady pro hierarchii zákazníků

Číselné řady v aplikaci slouží ke generování čitelných, jedinečných identifikátorů pro hlavní datové záznamy a záznamy transakcí, které požadují identifikátory. Musíte definovat číselnou řadu, která bude použita ke generování ID pro hierarchii zákazníků. Další informace o číselných řadách naleznete v tématu [Přehled číselných řad](/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview).

Chcete-li definovat číselnou řadu pro hierarchii zákazníků v centrále Commerce, postupujte následovně.

1. Přejděte na **Maloobchodní a velkoobchodní prodej \> Nastavení centrály \> Číselné řady \> Číselné řady**.
1. Vytvořte novou číselnou řadu nebo vyberte existující číselnou řadu a znovu ji použijte.
1. Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry \> Sdílené parametry obchodu**.
1. Na kartě **Číselné řady** přidejte číselnou řadu, kterou jste vytvořili nebo vybrali dříve, do reference **ID hierarchie zákazníků**.

![Číselná řada přidána do reference ID hierarchie zákazníka.](../media/NumberSequenceCustHierarchy.png)

## <a name="how-the-approval-process-works"></a>Jak funguje schvalovací proces

Když obchodní partner požádá o připojení k webu B2B elektronického obchodu, systém uloží požadavek jako *potenciálního zákazníka*. Osoba v centrále Commerce, například manažer maloobchodního provozu, může žádosti partnerů schválit nebo odmítnout. Další informace o správě požadavků obchodních partnerů a schvalování potenciálních zákazníků najdete v tématu [Správa uživatelů obchodních partnerů na webech elektronického obchodu B2B](manage-b2b-users.md).

Když je potenciální zákazník schválen, systém vytvoří dva nové záznamy o zákaznících:

- Jeden záznam zákazníka typu **Organizace** představuje organizaci, která se chce stát obchodním partnerem.
- Jeden záznam zákazníka typu **Osoba** představuje osobu, která žádost odeslala.

Kromě toho je vytvořen nový záznam hierarchie zákazníka ve stránce **Maloobchod a obchod \> Zákazníci \> Hierarchie zákazníků**. Tento záznam hierarchie zákazníků má následující vlastnosti:

- **ID hierarchie zákazníků** - Jedinečné ID hierarchie zákazníků. Toto ID používá číselnou sekvenci, kterou jste definovali ve sdílených parametrech Commerce.
- **Název** - Název organizace obchodního partnera, jak je uveden v žádosti o přihlášení. Toto pole je upravitelné.
- **Účel** - Tato vlastnost je nastavena na předdefinovanou hodnotu **B2B organizace**.
- **Organizace** - Zákaznické ID organizace obchodního partnera.

Osoba, která odeslala žádost o onboarding, je přidána na záložku **Hierarchie** a je jí přiřazena role **Správce**. Když správce přidá více uživatelů do organizace obchodního partnera na webu B2B, vytvoří se pro každého uživatele nový záznam zákazníka. Záznam zákazníka je také přidán do příslušného záznamu hierarchie zákazníků obchodního partnera a má přiřazenu roli **Uživatel**.

### <a name="examples"></a>Příklad

Osoba jménem Sam J. odešle žádost o onboarding jménem organizace Microsoft. Po schválení žádosti se vytvoří dva nové zákaznické účty: jeden typu **Osoba** pro Sama J. a jeden typu **Organizace** pro Microsoft.

Jak ukazuje příklad na následujícím obrázku, vytvoří se také nový záznam hierarchie zákazníka. Tento záznam má stejný název jako organizace (**Microsoft**), a uživateli Sam J. je přiřazena role **Správce**. Sam J. pak coby správce přidá do této hierarchie další uživatele webu B2B společnosti Microsoft a přiřadí jim roli **Uživatel**. V tomto příkladu byla jako uživatel přidána Sush R.

![Příklad záznamu hierarchie zákazníků.](../media/CustomerHierarchy2.png)

Chcete-li zjistit, zda je zákazník přidružen k hierarchii zákazníka, otevřete záznam zákazníka. Jak ukazuje příklad na následujícím obrázku, pole **ID zákaznické hierarchie** v sekci **B2B** na záložce **Maloobchod** ukazuje, zda je zákazník součástí zákaznické hierarchie, a možnost **Správce B2B** udává, zda je zákazník správcem dané hierarchie.

![Příklad sekce B2B na záložce Maloobchod záznamu zákazníka, kde je zákazník přidružen k hierarchii a určen jako správce.](../media/CustomerHierarchyMapping2.png)

Ve většině případů by se měly hodnoty vlastností všech záznamů zákazníků v hierarchii shodovat. Například proto, že všichni uživatelé obchodních partnerů by měli získat podobné ceny produktů, jejich cenová skupina a související konfigurace by se měly shodovat. Systém však tuto konzistenci nevynucuje. Příslušní uživatelé centrály Commerce jsou proto zodpovědní za zajištění shody hodnot vlastností a konfigurací pro všechny zákazníky v dané hierarchii.

Uživatelé centrály Commerce mohou kontrolovat hodnoty vlastností ve všech záznamech zákazníků v hierarchii v souběžném zobrazení. Jak ukazuje příklad na následujícím obrázku, můžete použít možnost **Obecné** v rozevíracím seznamu na záložce **Hierarchie** a poté vybrat libovolnou část záznamu zákazníka, aby se zobrazily související vlastnosti. Uživatelé mohou v tomto zobrazení přímo prohlížet hodnoty vlastností. Chcete-li zkopírovat všechny hodnoty ze zákaznického záznamu správce do všech uživatelů, vyberte **Přepsat** na záložce **Hierarchie**.

![Příklad záznamu hierarchie zákazníka zobrazující tlačítko Přepsat a možnost v rozevíracím seznamu.](../media/HierarchyDetails2.png)

[!include [footer-include](../../includes/footer-banner.md)]
