---
title: Úvod do funkčních míst
description: Toto téma obsahuje přehled funkčních míst v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationEditSubLocations, EntAssetFunctionalLocationLookup, EntAssetFunctionalLocationRename, EntAssetFunctionalLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80ea318d750f1ef18f270fa246ab54ecb63aa790
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888822"
---
# <a name="introduction-to-functional-locations"></a>Úvod do funkčních míst

[!include [banner](../../includes/banner.md)]

 

Toto téma obsahuje přehled funkčních míst v modulu Správa majetku. Funkční místa jsou prvky technické struktury, například funkční jednotky v systému. Funkční místa jsou vytvářena hierarchicky a vy na ně instalujete majetek. Nastavení funkčních míst ve vaší firmě závisí na požadavcích společnosti.

Zde je několik příkladů, jak můžete použít funkční místa:

- **Funkční** – Funkční místa mohou být orientovány na uživatele a slouží ke správě majetku, který má podobné chování.
- **Související s procesem** – Funkční místa mohou být orientována na workflow.
- **Prostorové** – Funkční místa mohou reprezentovat zeměpisné lokality nebo pracoviště.

Každé funkční místo je spravováno nezávisle v modulu Správa majetku. Zde jsou uvedeny některé z užitečných funkcí funkčních míst.

- Nastavte specifikace funkčních míst.
- Nastavte požadavky na specifikaci majetku.
- Nastavte pořadí údržby pro preventivní a reaktivní údržbu.
- Spravujte nainstalovaný majetek.
- Sledujte aktivní požadavky a pracovní příkazy, které souvisejí s nainstalovaným majetkem.
- Sledujte závady, které jsou registrovány u majetku.
- Sledujte náklady na údržbu majetku související s funkčním místem v kterémkoli daném okamžiku.

Funkční místa umožňují sledovatelnost majetku ve vztahu k požadavkům, pracovním příkazům, registracím poruch, vyhodnocování podmínek, registracím zastavení výroby a registracím čítačů majetku.

> [!NOTE]
> I když je majetek instalován na různých funkčních místech během jeho cyklu životnosti, náklady mohou souviset s každým místem. Jinými slovy, náklady na majetek jsou vždy spojeny s funkčním místem, ve kterém byl majetek instalován v daný čas.

Funkční místa **nejsou** flexibilní. Proto po nastavení hierarchie funkčních míst není možné přesouvat místa v této hierarchii. 

Po vytvoření hierarchie funkčních míst je dalším krokem instalace majetku v této hierarchii. Další informace najdete v části [Instalace majetku na funkčních místech](../functional-locations/install-objects-on-functional-locations.md).

## <a name="all-functional-locations"></a>Všechna funkční místa

Zvolte **Správa majetku** \> **Společné** \> **Funkční místa** \> **Všechna funkční místa** a otevřete stránku se seznamem **Všechna funkční místa**. Na této stránce jsou zobrazena všechna funkční místa a některé související informace. Chcete-li zobrazit pouze aktivní funkční místa, vyberte možnost **Aktivní funkční místa**. Chcete-li zobrazit pouze funkční místa, se kterými jste spojeni jako pracovník údržby, vyberte **Moje aktivní funkční místa**. (Tento vztah je nastaven na stránce **Pracovníci**. Další informace naleznete v tématu [Pracovníci údržby a skupiny pracovníků](../setup-for-objects/workers-and-worker-groups.md).)

Na stránce se seznamem **Všechna funkční místa** vyberte odkaz ve sloupci **Funkční místa**, chcete-li zobrazit podrobnosti o vybraném záznamu. Chcete-li upravit funkční místa, klikněte na tlačítko **Upravit**. V zobrazení podrobností jsou uvedeny podrobné informace vztahující se k místu. Obsahuje také podokno **Související informace** vpravo. V tomto podokně se zobrazuje hierarchie funkčních míst. Podokno **Související informace** můžete rozbalit nebo sbalit.

Tlačítka v podokně akcí jsou uspořádána na kartách. Následující tabulka stručně popisuje tlačítka, která souvisejí se správou majetku.

| Název tlačítka                         | Popis                                                                                                                                  |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Úpravy                                | Přepněte mezi režimem úprav a režimem zobrazení stránky.                                                                                         |
| Nové                                 | Vytvořte nové funkční místo.                                                                                                            |
| Odstranit                              | Odstraňte vybrané funkční místo.                                                                                                     |
| Přejmenovat                              | Přejmenujte vybrané funkční místo.                                                                                                     |
| Kopírování struktury funkčního místa  | Zkopírujte hierarchii funkčních míst.                                                                                                      |
| Instalace majetku                       | Instalujte majetek, včetně podřízeného majetku, do funkčního místa.                                                                        |
| Nahrazení majetku                       | Nahraďte hierarchii majetku jinou hierarchií majetku na funkčním místě.                                                         |
| Řízení nákladů                        | Otevřete stránku **Kontrola nákladů funkčního místa**, kde můžete provést výpočet nákladů pro vybrané funkční místo.                |
| Kontrola hodin                        | Otevřete stránku **Kontrola hodin funkčního místa**, kde můžete provést výpočet nákladů pro vybrané funkční místo.                |
| Prostředky                              | Otevřete stránku **Všechen majetek**, kde můžete zobrazit seznam majetku, který souvisí s vybraným funkčním místem.                      |
| Požadavky                            | Otevřete stránku **Aktivní požadavky**, kde můžete zobrazit seznam požadavků, který souvisí s vybraným funkčním místem.               |
| Pracovní příkazy                         | Otevřete stránku **Aktivní pracovní příkazy**, kde můžete zobrazit seznam pracovních příkazů, který souvisí s vybraným funkčním místem.         |
| Závady                              | Otevřete stránku **Závady majetku**, kde můžete zobrazit seznam registrací závad majetku, který souvisí s vybraným funkčním místem. |
| Aktualizace stavu funkčního místa    | Aktualizujte fázi vybraného funkčního místa.                                                                                        |
| Protokol stavu životního cyklu                 | Zobrazte protokol, který zobrazuje fáze vybraného funkčního místa.                                                                        |
