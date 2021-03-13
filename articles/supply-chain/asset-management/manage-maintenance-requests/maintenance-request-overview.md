---
title: Požadavky na údržbu
description: Toto téma obsahuje přehled správy požadavků na údržbu v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e0071ae745987a1217525b2841e3320933a9242
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019622"
---
# <a name="maintenance-requests"></a>Požadavky na údržbu

[!include [banner](../../includes/banner.md)]

 

Požadavky na údržbu jsou poznámky nebo prohlášení, které jsou vytvořeny za účelem upozornění manažera nebo plánovače, že majetek může vyžadovat úlohu údržby nebo opravy, ale bez vytvoření pracovního příkazu. Pokud je obsah požadavku na údržbu považován za platný, lze na základě požadavku na údržbu vytvořit pracovní příkaz.

Požadavky na údržbu mohou být vytvořeny pro libovolný majetek v modulu Správa majetku. V závislosti na způsobu použití požadavků na údržbu vaší společností lze vytvářet různé typy požadavků na údržbu. Několik příkladů:

- Požadavky na údržbu
- Poznámky
- Opravy nebo vylepšení
- Investice
- Oprava skladu (Tento typ se používá, když obdržíte majetek z jiného místa, aby bylo možné provést úlohu údržby nebo opravy a poté majetek vrátit po dokončení úlohy.)

## <a name="view-maintenance-requests"></a>Zobrazení požadavků na údržbu

Chcete-li zobrazit požadavky na údržbu, vyberte **Správa majetku** \> **Společné** \> **Požadavky na údržbu** \> **Všechny požadavky na údržbu**, **Aktivní požadavky na údržbu** nebo **Moje požadavky na údržbu funkčního místa**. Na každé stránce se seznamem jsou uvedeny některé informace související s požadavkem na údržbu.

![Zobrazit požadavky na údržbu](media/01-manage-maintenance-requests.png)

> [!NOTE]
> Použijte stránku se seznamem **Moje požadavky na údržbu funkčního místa** pro zobrazení seznamu požadavků na údržbu, které obsahují buď funkční místa, se kterými jste spojen jako pracovník, nebo majetek nainstalovaný ve funkčních místech, místěních, se kterým jste spojen jako pracovník (Informace o tom, jak nastavit funkční místa nebo pracovníky údržby, naleznete v tématu [Pracovníci údržby a skupiny pracovníků](../setup-for-objects/workers-and-worker-groups.md).)
> 
> Ačkoli jsou informace o účtu odběratele k dispozici ve správě služby majetku (externí údržba), nejsou k dispozici ve správě majetku (interní údržba).

Chcete-li otevřít zobrazení podrobností záznamu, na stránce se seznamem **Všechny požadavky na údržbu** v zobrazení mřížky vyberte odkaz ve sloupci **Požadavek na údržbu**.

![Zobrazení podrobností o požadavku na údržbu](media/02-manage-maintenance-requests.png)

Tlačítka v podokně akcí jsou uspořádána na kartách. Následující tabulka stručně popisuje tlačítka, která souvisejí se správou majetku.

| Název tlačítka                      | Popis |
|----------------------------------|-------------|
| Úpravy                             | Upravte vybraný požadavek na údržbu. |
| Nové                              | Vytvořte nový požadavku na údržbu. |
| Odstranit                           | Odstraňte zvolený požadavek na údržbu. |
| Fond pracovních příkazů                  | Připojte vybraný požadavek na údržbu k fondu pracovních příkazů. |
| Pracovní příkaz                       | Vytvořte pracovní příkaz na základě zvoleného požadavku na údržbu. |
| Závada majetku                      | Klikněte na **Závada majetku**, kde můžete vytvořit registraci poruch na vybraném požadavku na údržbu. |
| Pracovní příkazy                      | Zobrazte seznam všech pracovních příkazů, které jsou připojeny k vybranému požadavku na údržbu. |
| Aktualizace stavu požadavku na údržbu | Aktualizujte stav požadavku na údržbu. |
| Protokol stavu životního cyklu              | Zobrazí protokol, který zobrazuje stavy životního cyklu vybraného požadavku na údržbu. |
| Podrobnosti požadavku na údržbu      | Vytiskněte sestavu, která zobrazuje podrobnosti vybraného požadavku na údržbu. |
| Odeslání zapůjčeného majetku                  | Vyberte zapůjčený majetek, který by měl být dočasnou náhradou majetku vybraného na zvoleném požadavku na údržbu. |
| Vrácení vypůjčeného majetku                | Zaregistrujte zapůjčený majetek jako vrácený. |

