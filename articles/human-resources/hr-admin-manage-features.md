---
title: Správa funkcí v modulu Human Resources
description: Seznamte se s postupy zapnutí a vypnutí nových funkcí v aplikaci Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 80799b770f0ede9ca1175a44dd738ae635d012c2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793818"
---
# <a name="manage-features-in-human-resources"></a>Správa funkcí v modulu Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

V rámci našeho průběžného přidávání nových funkcí pro aplikaci Microsoft Dynamics 365 Human Resources chceme, aby zákazníci co nejdříve měli k dispozici nové funkce. Poskytujeme funkce Preview, které jsou téměř připraveny k obecné dostupnosti a prošly rozsáhlým testováním. Právě hledáme další z zpětnou vazbu od zákazníků a ověření před tím, než budou dostupné široké veřejnosti.

Další informace o nových funkcích v Human Resources naleznete v části [Co je nového v Human Resources](hr-admin-whats-new.md) a [plán vydání Dynamics 365 a Power Platform](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1).

Pracovní prostor **Správa funkcí** uvádí seznam funkcí dodaných v jednotlivých vydáních. Ve výchozím nastavení jsou nové funkce vypnuté. Pracovní prostor slouží k jejich zapnutí a zobrazení odpovídající dokumentace. Další informace o aktivaci správy funkcí naleznete v tématu [Přehled správy funkcí](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Všechny nové funkce zůstanou v náhledu nejméně 30 dnů a obvykle jsou zde 30-60 dní. Hlavní funkce jsou obvykle k dispozici v říjnu a dubnu každého roku po období náhledu. Jakmile se v pracovním prostoru **Správa funkcí** zobrazí nové funkce, můžete je zapnout. Některé funkce mohou být ve výchozím nastavení zapnuty.

Jakmile je funkce obecně k dispozici, může být zapnuta nebo vypnuta v provozních prostředích. Pracovní prostor **Správa funkcí** označuje, kdy bude funkce náhledu povinná. Toto datum je obvykle 1. října nebo 1. ledna, aby bylo možné vyrovnat je s pololetními plány vydávání. Nemůžete zapínat a vypínat povinné funkce. Dokud nebude povinná, můžete funkci zapnout nebo vypnout ve všech prostředích.

## <a name="enable-or-disable-preview-features"></a>Povolit nebo zakázat funkce náhledu

Chcete-li získat přístup k funkcím náhledu, je nutné je nejprve povolit ve vašem prostředí. Povolení nebo zakázání funkcí náhledu se vztahuje ke konkrétnímu prostředí.

> [!IMPORTANT]
> Funkce náhledu jsou k dispozici pouze v prostředích **Sandbox**. Když zapnete funkci Preview, povolíte ji pro všechny uživatele ve vaší organizaci, kteří jsou v prostředí. Vypnutím funkce Preview ji zakážete a způsobíte, že budou uživatelům nepřístupné. Funkce Preview mají v aplikaci Human Resources omezenou podporu. Mohou používat méně opatření pro soukromí a bezpečnostních opatření a nejsou zahrnuty do smlouvy o úrovni služeb (SLA) aplikace Human Resources. Neměli byste je používat ke zpracování osobních údajů (to znamená všech informací, které vás mohou identifikovat), nebo ke zpracování jiných dat, které podléhají požadavkům na vyhovění zákonům nebo předpisům.

1. V modulu Human Resources vyberte **Správa systému**.

2. Vyberte dlaždici **Správa funkcí**.

3. Chcete-li povolit funkci Preview, vyberte ji ze seznamu a poté vyberte možnost **Povolit**. Chcete-li zakázat funkci Preview, vyberte ji ze seznamu a poté vyberte možnost **Zakázat**.

## <a name="enable-or-disable-benefits-management"></a>Povolení nebo zákaz správy zaměstnaneckých výhod

Chcete-li povolit správu zaměstnaneckých výhod, použijte stejný postup při [povolení nebo zakázání funkcí náhledu](hr-admin-manage-features.md?enable-or-disable-preview-features).

> [!IMPORTANT]
> Správu zaměstnaneckých výhod v **Produkčním** prostředí nelze po povolení zakázat. Správu zaměstnaneckých výhod lze však zakázat v prostředích **Sandbox**.

Další informace o konfiguraci a použití správy zaměstnaneckých výhod naleznete v tématu [Přehled správy zaměstnaneckých výhod](hr-benefits-management-overview.md).

Správa zaměstnaneckých výhod nahrazuje funkce v pracovním prostoru **Zaměstnanecké výhody**. Pokud povolíte funkci Preview správy zaměstnaneckých výhod, nebude již možné získat přístup k následujícím formulářům v pracovním prostoru **Zaměstnanecké výhody**:

- **Zaměstnanecké výhody**
- **Prvky zaměstnanecké výhody**
- **Sazby pro výpočet příspěvku**
- **Výsledky přihlášení k zaměstnanecké výhodě**
- **Výsledky ukončení nebo prodloužení platnosti zaměstnanecké výhody**
- **Typy pravidel zásad nároků na zaměstnanecké výhody**
- **Zásady způsobilosti k zaměstnaneckým výhodám**
- **Události nároku**

Informace v těchto formulářích lze zobrazit v režimu jen pro čtení. Chcete-li upravit informace, je nejprve nutné zakázat funkci Preview správy zaměstnaneckých výhod (platí pouze pro prostředí **Sandbox**).

## <a name="enable-or-disable-leave-and-absence"></a>Povolit nebo zakázat Pracovní volno a absence

Chcete-li povolit Pracovní volno a absence, použijte stejný postup při [povolení nebo zakázání funkcí náhledu](hr-admin-manage-features.md?enable-or-disable-preview-features).

> [!IMPORTANT]
> Nemůžete zakázat fukci **Více typů pracovního volna** v Pracovní volno a absence po jejím povolení. to platí pro prostředí **Sandbox** i **Výroba**.

Další informace o funkcích náhledu v Pracovním volnu a absencích získáte v části [Funkce náhledu v pracovním volnu a absencích](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

## <a name="send-us-feedback"></a>Pošlete nám svůj názor

Rádi bychom se o vás dozvěděli něco o zkušenostech s funkcemi Preview. Doporučujeme vám pravidelně zveřejňovat zpětnou vazbu na následujících webech během používání těchto a dalších funkcí:

- [Komunita](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – tento web je skvělým zdrojem, kde mohou uživatelé diskutovat o případech použití, ptát se a získat nápovědu komunity.
- Dejte nám vědět, jaké funkce chcete zobrazit v produktu nebo o jakýchkoli změnách, které by měly podle vašeho názoru být provedeny u existujících funkcí. Navrhněte nápady týkající se produktů v [nápadech Human Resources](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources).
    
Neuvádějte ve zpětné vazbě nebo recenzích na produkty své osobní údaje (některé informace, které by vás mohly identifikovat). Shromážděné informace mohou být dále analyzovány a nebudou použity k odpovídání na žádosti v rámci platných zákonů o ochraně osobních údajů. Osobní údaje, které jsou získány samostatně v rámci těchto programů, se řídí [Prohlášením společnosti Microsoft o ochraně osobních údajů](https://privacy.microsoft.com/privacystatement).

## <a name="see-also"></a>Viz také

- [Co je nového v Human Resources](hr-admin-whats-new.md)
- [Plán vydání Dynamics 365 a Power Platform](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1)

[!INCLUDE[footer-include](../includes/footer-banner.md)]