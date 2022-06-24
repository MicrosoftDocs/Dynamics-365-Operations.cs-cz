---
title: Požadavky na údržbu
description: Tento článek obsahuje přehled správy požadavků na údržbu v modulu Správa majetku
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3d6f7861d5c242d512c4ac984e9e9f1d0890c5dc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848071"
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

![Zobrazit požadavky na údržbu.](media/01-manage-maintenance-requests.png)

> [!NOTE]
> Použijte stránku se seznamem **Moje požadavky na údržbu funkčního místa** pro zobrazení seznamu požadavků na údržbu, které obsahují buď funkční místa, se kterými jste spojen jako pracovník, nebo majetek nainstalovaný ve funkčních místech, místěních, se kterým jste spojen jako pracovník (Informace o tom, jak nastavit funkční místa nebo pracovníky údržby, naleznete v tématu [Pracovníci údržby a skupiny pracovníků](../setup-for-objects/workers-and-worker-groups.md).)
> 
> Ačkoli jsou informace o účtu odběratele k dispozici ve správě služby majetku (externí údržba), nejsou k dispozici ve správě majetku (interní údržba).

Chcete-li otevřít zobrazení podrobností záznamu, na stránce se seznamem **Všechny požadavky na údržbu** v zobrazení mřížky vyberte odkaz ve sloupci **Požadavek na údržbu**.

![Zobrazení podrobností o požadavku na údržbu.](media/02-manage-maintenance-requests.png)

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]