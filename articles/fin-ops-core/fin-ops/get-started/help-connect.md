---
title: Připojení k systému nápovědy
description: Toto téma popisuje součástí systému nápovědy pro aplikace Finance and Operations a poskytuje přehled o způsobu jejich propojení a shrnutí postupu pro vytvoření vlastní nápovědy.
author: margoc
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 491024c9c3d6c7d20ef212e167ceab6abac8dac7
ms.sourcegitcommit: d554faca895609b8124bf2ea5aca5a55c407534a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/02/2019
ms.locfileid: "2537848"
---
# <a name="connect-the-help-system"></a>Připojení k systému nápovědy

[!include [banner](../includes/banner.md)]

V tomto tématu jsou popsány komponenty systému nápovědy pro aplikace Finance and Operations, jako je Dynamics 365 Finance, Supply Chain Management, Retail a Talent. Poskytuje přehled o tom, jak připojit tyto komponenty, a souhrnné informace o tom, jak vytvořit vlastní nápovědu.

## <a name="help-architecture"></a>Architektura nápovědy

Následující obrázek znázorňuje části systému nápovědy. Systém nápovědy v produktu přebírá články z webu https://docs.microsoft.com a také z průvodců záznamem úloh uložených v modulu Modelování podnikových procesů ve službě Lifecycle Services (LCS).

> [!NOTE]
> Funkce označené v diagramu hvězdičkou (\*) jsou plánované, ale nejsou zatím k dispozici.

[![Architektura nápovědy](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Připojení systému nápovědy

> [!NOTE]
> Karta **Průvodci záznamem** úloh není k dispozici v aplikacích Dynamics 365 Talent či Retail. Funkci zpřístupníme v budoucí verzi. Průvodci v prostředí Začínáme v aplikaci Talent jsou i nadále k dispozici a zabývají se základními funkcemi. Procesní nápověda je k dispozici také na webu docs.microsoft.com pro Retail a Talent.

Pomocí stránky **Systémové parametry** správci systému připojí části systému nápovědy pro implementaci.

[![Formulář Systémové parametry s nastavením nápovědy](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

Na stránce **Systémové parametry** proveďte následující kroky:

> [!IMPORTANT]
> Při prvním otevření karty **Nápověda** je nutné se připojit k službě Lifecycle Services. Klikněte na odkaz uprostřed formuláře, počkejte na připojení, zavřete dialogové okno a kliknutím na tlačítko **OK** otevřete stránku **Parametry** systému.
>
> [![Připojení k LCS](./media/connect-to-lcs-crop-1024x365.png "Připojení k LCS")](./media/connect-to-lcs-crop.png)

1. Vyberte projekt služby Lifecycle Services pro připojení.
2. Vyberte knihovny BPM (v rámci vybraného projektu), ze kterých chcete načíst záznamy úkolů.
3. Nastavte pořadí zobrazení knihoven BPM. Tato možnost určuje pořadí, ve kterém se záznamy úkolů z knihoven zobrazí v podokně **Nápověda**.

Po dokončení těchto kroků můžete otevřít podokno **Nápověda** a kliknutí na kartu **Průvodci záznamem úloh**. Zobrazí se vám nyní průvodci záznamem úloh, které se vztahují ke stránce, na které se momentálně v aplikacích Finance and Operations nacházíte. Pokud nebyly nalezeny žádné průvodce úkolem, můžete zadat klíčová slova pro upřesnění hledání.

### <a name="showing-translated-task-guides"></a>Zobrazení přeložených průvodců úkoly

Přeložení průvodci úkolem byli poprvé vydání v knihovně APQC Unified Library pro květen 2016 a v knihovně Začínáme. Chcete-li v aplikacích Finance and Operations zobrazit lokalizovanou nápovědu k průvodci záznamem úloh, zkontrolujte, zda máte připojenou knihovnu z května. Jazyk, ve kterém se průvodce úkolem zobrazí, je řízen pro každého uživatele v jazykovém nastavení v části **Možnosti** &gt; **Předvolby**.

> [!NOTE]
> I když mnoho průvodců úkolem již bylo přeloženy, klient aktuálně nezobrazuje názvy přeložených průvodců úkolem. Stejně tak pouze průvodci úkolem vydaní v únoru jsou momentálně k dispozici v překladu v knihovně pro únor 2016. Aktualizovanou knihovnou s další překlady zpřístupníme později.
>
> - Pokud průvodce úkolem byl přeložen, veškerý text průvodce úkolem se při otevření daného průvodce zobrazí ve vybraném jazyce.
> - Pokud průvodce úkolem zatím nebyl přeložen, při otevření daného průvodce se zobrazí ve vybraném jazyce pouze některý text (text ovládacích prvků).

## <a name="creating-custom-help"></a>Vytváření vlastních nápověd

Můžete použít průvodce záznamem úloh k vytvoření vlastní nápovědy, nebo připojit své webové stránky k panelu Nápověda.

### <a name="create-custom-help-with-task-guides"></a>Vytvoření vlastní nápovědy pomocí průvodců záznamem úloh

Vlastní nápovědu pro aplikace Finance, Supply Chain Management a Retail můžete vytvořit tak, že vytvoříte záznamy úloh, které odpovídají vaší implementaci, a uložíte je do knihovny obchodního procesu LCS. Pro aplikaci Talent nelze vlastní průvodce záznamem úloh vytvořit.

Pro partnery platí, že pokud knihovnu nastavíte jako podnikovou knihovnu a zahrnete ji do řešení, bude k dispozici vašim odběratelům. Můžete vytvořit také kopii sjednocené globální knihovny APQC a poté otevřít kopii z ní otevřít záznamy úloh, upravit je a uložit záznamy s provedenými změnami. Další informace naleznete v tématu [Vytvoření záznamu úkolu jako dokumentace nebo školení](../../dev-itpro/user-interface/task-recorder.md).

### <a name="connect-a-custom-site"></a>Připojení vlastního webu

Společnost Microsoft poskytla dokument white paper a vzorový kód, které popisují způsob vytvoření a připojení vlastního webu nápovědy k panelu Nápověda. Další informace naleznete zde:

- [Vytvoření vlastní nápovědy pro aplikace Finance and Operations (dokument white paper)](https://go.microsoft.com/fwlink/?linkid=2041185)
- [Úložiště GitHub vlastní nápovědy](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a>Další zdroje

[Přehled nápovědy](help-overview.md)

[Přehled záznamníku úloh](../../dev-itpro/user-interface/task-recorder.md)

[Postup vytvoření záznamu úloh pro použití jako dokumentace nebo školení](../../dev-itpro/user-interface/task-recorder-training-docs.md)