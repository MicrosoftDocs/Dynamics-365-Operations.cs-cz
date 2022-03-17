---
title: Import funkcí z globálního úložiště
description: Toto téma vysvětluje, jak importovat funkce globalizace z globálního úložiště.
author: dkalyuzh
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: ff3019986d089a286f7aef94346398b3d328ad54
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371549"
---
# <a name="import-features-from-the-global-repository"></a>Import funkcí z globálního úložiště

[!include [banner](../includes/banner.md)]

Globální úložiště obsahuje funkce Elektronické fakturace, které jsou sdíleny s vaším poskytovatelem konfigurace. Všechny funkce Elektronické fakturace poskytované společností Microsoft jsou sdíleny se všemi společnostmi. Automaticky máte přístup ke všem funkcím Elektronické fakturace, které společnost Microsoft vydává a publikuje v globálním úložišti.

Chcete-li začít pracovat s funkcemi Elektronické fakturace, které jsou sdíleny s vaším poskytovatelem konfigurace, importujte je do své instance Regulatory Configuration Service (RCS) z globálního úložiště. Pak si přečtěte podrobnosti o funkci, jako jsou konfigurace elektronického hlášení (ER) a kanály zpracování.

## <a name="import-a-feature-from-the-global-repository"></a>Import funkce z globálního úložiště

1. Přihlaste se k účtu RCS.
2. V pracovním prostoru **Funkce globalizace** v části **Funkce** vyberte dlaždici **Elektronická fakturace**.
3. Výběrem možnosti **Import** otevřete vyhledávání **Import funkce z globálního úložiště**.
4. Chcete-li procházet funkce Elektronické fakturace, které jsou k dispozici v globálním úložišti pro konkrétního poskytovatele konfigurace, synchronizujte instanci RCS vaší organizace výběrem položky **Synchronizovat**. Po dokončení synchronizace se aktualizuje seznam dostupných funkcí Elektronické fakturace z globálního úložiště. Tato aktualizace může trvat několik minut.
5. Vyberte funkci, kterou chcete importovat, a poté vyberte **Import**.

Chcete-li zobrazit importovanou funkci Elektronické fakturace, zkontrolujte, že je vybrán správný poskytovatel konfigurace. Ve výchozím nastavení jsou funkce vytvořené poskytovatelem aktivní konfigurace automaticky odfiltrovány. Filtr můžete upravit tak, aby se zobrazovaly funkce, které byly vytvořeny jinými poskytovateli, jako je poskytovatel konfigurace Microsoft.

Nyní můžete pracovat s importovanou funkcí. Můžete zkontrolovat její podrobnosti a vytvořit novou funkci pomocí importované funkce jako šablony.

> [!NOTE]
> Funkci můžete upravit, pouze pokud byla vytvořena poskytovatelem konfigurace, který je aktuálně aktivní. Můžete vytvořit novou funkci s využitím původní funkce jako základu. Poté můžete provést požadované změny nebo nastavit parametry.

Když společnost Microsoft nebo jiná společnost, která sdílí funkce globalizace s vaší společností, aktualizuje funkce, které jste importovali, můžete vyhledat aktualizované verze výběrem příkazu **Zkontrolovat aktualizace funkce** v sekci **Související nastavení** pracovního prostoru **Funkce globalizace**.

Pokud vidíte, že existují aktualizace pro funkci, kterou používáte jako šablonu, můžete po synchronizaci seznamu publikovaných funkcí v globálním úložišti importovat novou verzi.
