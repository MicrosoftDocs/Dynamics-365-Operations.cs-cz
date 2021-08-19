---
title: Zodpovědní pracovníci údržby
description: Toto téma vysvětluje, jak nastavit zodpovědné pracovníky údržby v modulu Správa majetku.
author: johanhoffmann
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkerResponsible
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d68c9e6de6e9d62d1dea95c747b17900d343e7324857dcfc083d48e5c1006b0e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731288"
---
# <a name="responsible-maintenance-workers"></a>Zodpovědní pracovníci údržby

[!include [banner](../../includes/banner.md)]

 

Zodpovědní pracovníci údržby mohou být spřízněni s typy majetku, majetkem, funkčními místy, kategoriemi typů údržby, typy prací údržby, variantami typů prací údržby a obchody. Mohou být použity v pracovních příkazech a požadavcích na údržbu, aby označovali preference týkající se pracovníků údržby, kteří by měli být zodpovědní za pracovní příkaz. (Tito pracovníci údržby však nemusí být nutně stejnými zaměstnanci, kteří mají v plánu provést pracovní příkaz.) Použití této funkce je nepovinné. Lze jej například použít k výběru odpovědných pracovníků nebo skupin pracovníků pro určité typy práce nebo pracovní oblasti.

Během životního cyklu pracovního příkazu nebo životního cyklu požadavků na údržbu je možné změnit nebo aktualizovat zodpovědné pracovníky údržby. Tato změna nebo aktualizace může souviset například se změnou stavu životního cyklu požadavku na údržbu nebo stavem životního cyklu pracovního příkazu.

Nastavení na stránce **Zodpovědní pracovníci údržby** se *nepoužívá* během plánování pracovního příkazu.

> [!NOTE]
> V modulu Správa majetku můžete také nastavit *upřednostňované* pracovníky údržby, kteří mohou být během plánování pracovních příkazů přidělovány do pracovních příkazů.

Před nastavením zodpovědných pracovníků údržby je nutné nastavit pracovníky a skupiny pracovníků údržby, kteří by měli být k dispozici pro výběr. Informace o tom, jak nastavit skupiny zaměstnanců a pracovníků údržby, naleznete v tématu [Pracovníci údržby a skupiny pracovníků](../setup-for-objects/workers-and-worker-groups.md).

## <a name="set-up-responsible-maintenance-workers"></a>Nastavit odpovědné pracovníky údržby

1. Vyberte **Správa majetku** \> **Nastavení** \> **Pracovníci** \> **Zodpovědní pracovníci údržby**.
2. Zvolte **Nový** pro vytvoření záznamu.
3. Nejprve vytvořte výchozího zodpovědného pracovníka údržby, který je odpovědný za údržbu, a v níž nastavíte pouze pole **Skupina zodpovědných pracovníků údržby** a/nebo pole **Zodpovědný pracovník**. Zbývající pole ponechejte prázdná. Toto výchozí nastavení bude použito během plánování pracovního příkazu, pokud žádná jiná specifická kombinace neodpovídá obsahu pracovního příkazu.

    > [!NOTE]
    > Při vytváření žádosti o údržbu, kdy je odpovědný pracovník údržby nebo odpovědná skupina pracovníků údržby zpřístupněna pro výběr na stránce **Všechny požadavky na údržbu**, bude správa majetku procházet všemi záznamy odpovědných pracovníků údržby, aby bylo možné vyhledat možnou shodu. Vždy zkontroluje nejdříve nejkonkrétnější kombinaci. Jinými slovy, Správa majetku nejprve zkontroluje shodu v poli **Obchod**. Pokud není nalezena shoda, zkontroluje shodu v poli **Varianta typu práce údržby**. Pokud není nalezena shoda, zkontroluje shodu v poli **Typ práce údržby** a tak dále. Jak je vidět v rozvržení stránky, toto chování znamená, že pro nalezení nejspecifičtější kombinace kontroluje Správa majetku každý záznam zprava doleva pro shodu (nejprve **Obchod**, pak **Varianta typu práce údržby**, pak **Typ práce údržby**, pak **Kategorie typu práce údržby**, pak **Funkční místo**, potom **Majetek** a nakonec **Typ majetku**). Není-li nalezena shoda, použije se výchozí záznam, který nemá žádné výběry v těchto sedmi polích.

Následující ilustrace znázorňuje příklad stránky **Zodpovědní pracovníci údržby**.

![Stránka Zodpovědní pracovníci údržby.](media/08-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]