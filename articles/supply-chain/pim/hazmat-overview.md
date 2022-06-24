---
title: Přehled nebezpečných materiálů
description: Tento článek poskytuje přehled funkcí, které souvisejí s manipulací a dokumentací nebezpečných materiálů během správy informací o produktu a správy skladu.
author: t-benebo
ms.date: 06/10/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: c2cae4cb65dd163e9fbf1d24cff5a0a040e3ce3a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905798"
---
# <a name="hazardous-materials-overview"></a>Přehled nebezpečných materiálů

[!include [banner](../includes/banner.md)]

Aby organizace, které přepravují materiály klasifikované jako nebezpečné zboží, dodržovaly přepravní předpisy, musí ke svým zásilkám přiložit dodatečné doklady. Funkce nebezpečných materiálů umožňuje zákazníkům ukládat informace související s uvolněnými položkami. Tyto informace lze poté použít k přípravě dokumentace o dodávce. Organizace, která přepravuje nebezpečné zboží, musí mít vlastní procesy a postupy pro správu přepravního procesu. Microsoft Dynamics 365 Supply Chain Management je jen nástroj, který může pomoci vygenerovat požadované dokumenty.

Následující diagram znázorňuje kroky potřebné k nastavení a používání funkce nebezpečných materiálů.

![Nastavení a použití funkce nebezpečných materiálů.](media/hazmat-overview.png "Nastavení a použití funkce nebezpečných materiálů")

Funkce nebezpečných materiálů je nastavena ve správě informací o produktu a poskytuje dokumenty, které lze vytisknout prostřednictvím správy skladu. Obecně řečeno, tyto oblasti jsou dvě hlavní oblasti, kde budete kontrolovat, nastavovat a používat tuto funkci:

- **Správa informací o produktech** – Nastavení kódů, které budou použity na uvolněný produkt.
- **Řízení skladu** – Práce s dodatečnými dodacími doklady, které budou pro zásilky vytištěny.

> [!IMPORTANT]
> Funkce nebezpečných materiálů v modulu Supply Chain Management poskytují kolekci užitečných polí s informacemi o produktu a souvisejících funkcích, které vám mohou pomoci zaznamenat a odkazovat na informace související s vašimi nebezpečnými produkty. Tyto funkce vám také mohou pomoci navrhnout a vytisknout dodací doklady, které obsahují některé totožné informace o všech nebezpečných materiálech, které přepravujete. Systém však automaticky nezajistí vaši plnou kompatibilitu se všemi platnými regulacemi vaší země nebo oblasti. Ačkoli jsou tyto nástroje určeny k tomu, aby vám pomohly dodržovat společné předpisy, nejsou samy o sobě dostatečné ani zaručené. Vaše organizace je odpovědná za to, že si je vědoma všech příslušných předpisů a že podniká všechny kroky nezbytné k jejich dodržování.

## <a name="product-information-management"></a>Řízení informací o produktech

Správa informací o produktu poskytuje řadu nastavení tabulek, kde můžete zadat referenční informace pro různé seznamy nebezpečného zboží pro silniční, leteckou a námořní dopravu.

Při vývoji této funkce se počítalo s následujícími společnými předpisy:

- **ADR** – Nařízení vztahující se k mezinárodní přepravě nebezpečného zboží po silnici
- **CFR 49** - Nařízení v USA pro přepravu nebezpečného zboží
- **IMDG** – Kód mezinárodní námořní přepravy nebezpečného zboží
- **IATA** – Nařízení mezinárodního sdružení letecké dopravy (IATA) o nebezpečném zboží

Každá sada předpisů poskytuje standardizované seznamy nebezpečných zboží a referenční kódy. Proto Supply Chain Management poskytuje referenční tabulku pro společné kódy v těchto seznamech. Každý seznam obsahuje také některé jedinečné kódy, které můžete definovat.

Další informace, jak nastavit předpisy a hodnoty pro nebezpečné materiály a jak přiřadit hodnoty příslušným produktům, najdete v následujících článcích:

- [Příprava nebezpečných materiálů](hazmat-setup.md)
- [Nebezpečné materiály ve výrobcích, objednávkách, dodávkách a nákladech](hazmat-items.md)

## <a name="warehouse-management"></a>Řízení skladu

Když připravujete dodávku v Řízení skladu, můžete vytisknout několik nových sestav, které používají informace, které jste nastavili v Řízení informací o produktech. Další informace o dostupných sestavách a jejich použití najdete v části [Nebezpečné materiály – dotazy a sestavy](hazmat-reports.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]