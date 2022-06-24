---
title: Nastavení skladu s použitím šablony konfigurace skladu
description: Tento článek vysvětluje nastavení skladu s použitím šablony konfigurace skladu.
author: yufeihuang
ms.date: 11/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportEnhanced, DMFDefinitionGroupTemplate, DMFEntityTemplateDefinitionLoadDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 737b6f2f645ff270e5a49d54ca7542df3c075f94
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856099"
---
# <a name="set-up-a-warehouse-by-using-a-warehouse-configuration-template"></a>Nastavení skladu s použitím šablony konfigurace skladu

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje nastavení skladu s použitím šablony konfigurace skladu. Existuje několik předdefinovaných šablon konfigurace, které lze použít. Další informace o použití hodnot těchto šablon naleznete v tématu [Šablony dat konfigurací](../../fin-ops-core/dev-itpro/data-entities/configuration-data-templates.md).

## <a name="scenarios-where-configuration-templates-can-be-helpful"></a>Scénáře, které mohou být šablony konfigurací užitečné

Šablony konfigurací mohou být užitečné v mnoha scénářích. Několik příkladů:

- Dokončili jste a otestovali nastavení konfigurace v testovacím prostředí a nyní chcete kopírovat nastavení do provozního prostředí.
- Chcete zavést nastavení skladu pro více právnických osob nebo vytvořit nový sklad ve stejné právnické osobě.
- Chcete se rychle připravit na ukázku funkcí skladu.
- Chcete, aby existující položky a sklady používaly funkce v modulu Řízení skladu namísto funkce v modulu Řízení zásob.

Tento článek se zaměřuje na první z těchto scénářů. Ukazuje použití šablony konfigurace pro zkopírování nastavení konfigurace z testovacího prostředí do provozního prostředí.

## <a name="copy-a-configuration-setup-from-a-test-environment-to-a-production-environment"></a>Kopírování nastavení konfigurace z testovacího prostředí do provozního prostředí

V tomto scénáři již existují v testovacím prostředí nastavení konfigurace pro sklad a některé procesy transakce. Nyní chcete kopírovat nastavení konfigurace pro sklad z testovacího prostředí do provozního prostředí.

> [!NOTE]
> Je důležité, abyste zahrnuli další související data nastavení při kopírování nastavení konfigurace. Chcete například nastavit produkty zkopírováním nastavení z testovacího prostředí. Nelze však nastavit pevně stanovené výdejní skladové místo pro produkt před vytvořením produktu. Ačkoliv jednotlivé šablony konfigurace nepodporují tento typ závislosti, existují výchozí šablony dat, které ho podporují. Tyto výchozí šablony dat lze snadno zahrnout do procesu konfigurace.

### <a name="export-a-default-warehouse-template"></a>Export výchozí šablony skladu 

1. Otevřete pracovní prostor **Správa dat**.

    > [!NOTE]
    > Pokud používáte tento pracovní prostor poprvé, je nutné načíst všechny entity dat předtím, než budete pokračovat.

2. Vyberte dlaždici **Šablony** a poté vyberte **Načíst výchozí šablony** pro načtení výchozích šablon.

    > [!NOTE]
    > Možnost **Načíst výchozí šablony** je dostupné pouze v zobrazení **Rozšířené**. Vyberte **Parametry architektury** a poté v poli **Zobrazit výchozí** vyberte **Rozšířené zobrazení**.

3. Poté, co jsou načteny výchozí šablony, je lze změnit tak, aby splňovaly vaše obchodní požadavky.

    > [!NOTE]
    > Abyste mohli načíst výchozí šablony a importovat je, musíte mít přístup správce systému. Tento požadavek pomáhá zaručit, že se všechny šablony načtou do šablony správně.

4. Ujistěte se, že se nacházíte v právnické osobě, ze které chcete exportovat data specifická pro společnost.
5. V pracovním prostoru vyberte **Exportovat**.
6. Vytvořte nový projekt exportu.
7. Vyberte **+ Přidat šablonu** a vyhledejte výchozí šablonu skladu **400 - WMS**. Tato šablona přidá entity dat pro konfiguraci skladu.

    > [!NOTE]
    > Je-li nutné filtrovat exportovaná data (například chcete exportovat pouze data, která souvisí s určitým skladem), je nutné vyhodnotit každou datovou entitu a přidat filtrování pomocí dotazu. Případně můžete exportovat všechna data a potom odstranit záznamy, které nejsou vyžadovány v cílových souborech.

8. Vyberte **Export**. Jsou exportována data, která se vztahují ke všem datovým entitám v projektu.

U datového balíčku můžete stáhnout soubor ZIP. Tento soubor obsahuje všechna data ve vybraném formátu (například formát aplikace Excel). Jak bylo zmíněno, některé záznamy v souborech datových balíčků může být zapotřebí aktualizovat před jejich importem do provozního prostředí. Při aktualizaci záznamu se ujistěte se, že nezměníte název souboru.

### <a name="import-a-warehouse-configuration-setup"></a>Import nastavení konfigurace skladu

1. V cílovém prostředí se ujistěte, že se nacházíte ve společnosti, do které chcete importovat data skladu.

    > [!NOTE]
    > Před provedením importu je nutné určit závislosti dat. Například šablona **Řízení skladu** obsahuje datovou entitu s názvem **Dispoziční kódy skladu**. Tato entita obsahuje data, která souvisí s nastavením stránky **Dispoziční kódy** (**Řízení skladu** > **Nastavení** > **Mobilní zařízení** > **Dispoziční kódy**). Pokud již existující nastavení zpracovává proces vrácení prodejních objednávek , pole **Vrátit dispoziční kód** obsahuje hodnotu. Dispoziční kód v tomto poli se vztahuje k datové entitě **Dispoziční kód**, která je součástí šablony **Prodeje a marketing**. Pokud data z datové entity **Dispoziční kód** nejsou importována dříve než data z pole **Dispoziční kódy skladu**, import se nezdaří.

2. V pracovním prostoru **Správa dat** vyberte **Importovat**.
3. Vytvořte nový projekt importu.
4. Vyberte **+ Přidat soubor** a odešlete soubor ZIP pro datový balíček.
5. Vyberte **Import**. V zobrazení **Rozšířené** můžete použít možnost **Filtr**, abyste rychle získali přehled o problémech, které mohou nastat během importu.

Možnost **Zobrazit protokol provádění** obsahuje podrobné informace o každé datové entitě, která je importována. Můžete použít zobrazení dat fázování, abyste se dostali rychle k cílovým datům. V takovém případě se zobrazí, jak vypadají importovaná data na souvisejících stránkách v aplikaci. Při použití výchozích datových šablon pracuje pořadí importu pro každou datovou entitu předem definovaným způsobem, aby se zajistilo, že všechna závislá data budou importována nejdříve. Jsou-li vlastní datové entity součástí projektu, je třeba zkontrolovat, že je definováno správné pořadí. Další informace naleznete v tématu[Šablony dat konfigurací](../../fin-ops-core/dev-itpro/data-entities/configuration-data-templates.md).

Chcete-li se dozvědět více o tom, jak používat šablonu skladu pro zkopírování konfigurace skladu z jedné společnosti do nové společnosti ve stejné instanci, podívejte se na toto 3minutové video na YouTube nazvané [Použití šablony skladu ke kopírování konfigurace v aplikaci Finance and Operations](https://www.youtube.com/watch?v=K2WIfFlqJYs).

## <a name="related-article"></a>Související článek

[Šablony dat konfigurací](../../fin-ops-core/dev-itpro/data-entities/configuration-data-templates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]