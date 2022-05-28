---
title: Archivace skladových transakcí
description: Toto téma popisuje, jak archivovat data skladových transakcí za účelem zlepšení výkonu systému.
author: yufeihuang
ms.date: 05/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8b766d306f31fc531f33aa29e1f96048bbd90085
ms.sourcegitcommit: e18ea2458ae042b7d83f5102ed40140d1067301a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2022
ms.locfileid: "8736054"
---
# <a name="archive-inventory-transactions"></a>Archivace skladových transakcí

[!include [banner](../../includes/banner.md)]

V průběhu času bude tabulka skladových transakcí (`InventTrans`) i nadále růst a zabírat více prostoru v databázi. Proto se dotazy spouštěné proti této tabulce postupně zpomalí. Toto téma popisuje, jak můžete používat funkci *Archivace skladových transakcí* pro archivaci dat o skladových transakcích, která pomůže zlepšit výkon systému.

> [!NOTE]
> Ve vybraném uzavřeném období hlavní knihy lze archivovat pouze finančně aktualizované skladové transakce. Finančně aktualizované odchozí skladové transakce, které chcete archivovat, musejí mít stav výdeje s hodnotou *Prodáno*, a příchozí skladové transakce musejí mít stav přijetí *Zakoupeno*.

Když archivujete skladové transakce, všechny související transakce se přesunou do tabulky `InventTransArchive`. Transakce výdeje ze skladu a transakce příjmu na sklad se archivují samostatně na základě kombinace ID položky (`itemId`) a ID dimenze zásob (`inventDimId`), a jsou vloženy do transakcí souhrnného výdeje a souhrnných příjmů.

Když kombinace `itemId` a `inventDimId` obsahuje pouze jednu transakci příjmu nebo výdeje, transakce nebude archivována.

## <a name="turn-on-the-feature-in-your-system"></a>Zapnutí funkce ve vašem systému

Pokud váš systém ještě neobsahuje funkce popsané v tomto tématu, přejděte na stránku [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapněte funkci *Archivace skladových transakcí*. Tuto funkci nelze deaktivovat, jakmile bude povolena.

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a>Co je třeba zvážit před archivací skladových transakcí

Před archivací skladových transakcí byste měli zvážit následující obchodní scénáře, protože budou touto operací ovlivněny:

- Když auditujete skladové transakce ze souvisejících dokumentů, jako jsou řádky nákupní objednávky, zobrazí se jako archivované. Chcete-li zkontrolovat archivované transakce, musíte přejít do nabídky **Řízení zásob \> Pravidelné úkoly \> Vyčistit \> Archivace skladových transakcí**.
- Uzávěrku skladu nelze zrušit pro archivovaná období. Než budete moci zrušit uzávěrku inventáře, musíte stornovat archivaci skladových transakcí pro příslušné období.
- Standardní konverzi nákladů nelze provést pro archivovaná období. Než budete moci provést standardní konverzi nákladů, musíte stornovat archivaci skladových transakcí pro příslušné období.
- Sestavy zásob, které vycházejí ze skladových transakcí, budou při archivaci skladových transakcí ovlivněny. Mezi tyto sestavy patří sestava prodlení zásob a sestavy hodnoty skladu.
- Prognózy zásob mohou být ovlivněny, pokud jsou spuštěny v časovém horizontu archivovaných období.

## <a name="prerequisites"></a>Předpoklady

Skladové transakce lze archivovat pouze během období, kdy jsou splněny následující podmínky:

- Období hlavní knihy musí být uzavřeno.
- Uzávěrka zásob musí být spuštěna k datu archivu Období do nebo po něm.
- Období musí být nejméně jeden rok před datem archivu Období od.
- Nesmí existovat žádné stávající přepočty skladu.

## <a name="archive-inventory-transactions"></a>Archivace skladových transakcí

Chcete-li archivovat skladové transakce, postupujte takto.

1. Přejděte do nabídky **Řízení zásob** \> **Pravidelné úkoly** \> **Vyčistit** \> **Archivace skladových transakcí**.

    Zobrazí se stránka **Archivace skladových transakcí** se seznamem archivovaných záznamů procesu.

    ![Stránka Archivace skladových transakcí.](media/archive-inventory-empty.png "Stránka Archivace skladových transakcí")

1. V podokně akcí vyberte příkaz **Archivace skladových transakcí** pro vytvoření archivu skladových transakcí.
1. V dialogovém okně **Archivace skladových transakcí** na záložce **Parametry** nastavte následující pole:

    - **Od data v uzavřeném účetním období** - Vyberte nejstarší datum transakce, které chcete zahrnout do archivu.
    - **Do data v uzavřeném účetním období** - Vyberte nejnovější datum transakce, které chcete zahrnout do archivu.

    ![Dialogové okno Archivace skladových transakcí.](media/archive-inventory-dates.png "Dialogové okno Archivace skladových transakcí")

    > [!NOTE]
    > Vybrat bude možné pouze období, která splňují [předpoklady](#prerequisites).

1. Na záložce **Spustit na pozadí** nastavte detaily dávkového zpracování podle potřeby. Postupujte podle obvyklých kroků pro dávkové úlohy v Microsoftu Dynamics 365 Supply Chain Management.
1. Vyberte **OK**.
1. Zobrazí se zpráva s výzvou k potvrzení, že chcete pokračovat. Přečtěte si pozorně zprávu a poté vyberte **Ano**, pokud chcete pokračovat.

    Zobrazí se zpráva, že vaše úloha archivace skladových transakcí byla přidána do fronty dávek. Úloha nyní začne archivovat skladové transakce od vybraného období.

## <a name="view-archived-inventory-transactions"></a>Zobrazit archivované transakce zásob

Stránka **Archivace skladových transakcí** zobrazuje vaši úplnou historii archivace. Každý řádek v mřížce zobrazuje informace, jako je datum vytvoření archivu, jméno uživatele, který jej vytvořil, a jeho stav.

![Historie archivace na stránce Archivace skladových transakcí.](media/archive-inventory-full.png "Historie archivace na stránce Archivace skladových transakcí")

Chcete-li filtrovat archivy zobrazené v mřížce, vyberte v rozevíracím seznamu v horní části stránky jednu z následujících hodnot:

- **Aktivní** – Zobrazí pouze aktivní archivy, nikoli stornované archivy.
- **Vše** – Zobrazí všechny archivy, aktivní i stornované.

U každého archivu v mřížce jsou k dispozici následující informace:

- **Aktivní** – Zaškrtnutí označuje, že archiv je aktivní.
- **Od data** – Datum nejstarší transakce, kterou lze zahrnout do archivu.
- **Do data** – Datum nejnovější transakce, kterou lze zahrnout do archivu.
- **Naplánoval(a)** – Uživatelský účet, který vytvořil archiv.
- **Provedeno** – Datum vytvoření archivu.
- **Stornováno** – Zaškrtnutí označuje, že archiv byl stornován.
- **Zastavit aktuální aktualizaci** – Zaškrtnutí označuje, že archivace právě probíhá, ale byla pozastavena.
- **Stav** – Stav zpracování archivu. Možné hodnoty jsou *Čekání*, *Probíhá*, a *Dokončeno*.

Panel nástrojů nad mřížkou poskytuje následující tlačítka, která můžete použít k práci s vybraným archivem:

- **Archivované transakce** – Zobrazí všechny podrobnosti o vybraném archivu. Stránka **Archivované transakce**, která se zobrazí, ukazuje všechny transakce v archivu.

    ![Stránka archivovaných transakcí.](media/archive-inventory-transactions.png "Stránka archivovaných transakcí")

    Chcete-li zobrazit více informací o konkrétní transakci na stránce **Archivované transakce**, vyberte ji v mřížce a poté v podokně akcí vyberte **Detaily archivované transakce**. Stránka **Detaily archivované transakce**, která se zobrazí, ukazuje například účtování do hlavní knihy, související odkazy na dílčí hlavní knihu a finanční dimenze.

- **Pozastavit archivaci** – Pozastaví vybraný archiv, který se právě zpracovává. Pauza se projeví až po vygenerování úlohy archivace. Proto může dojít k krátkému zpoždění, než se pozastavení projeví. Pokud byl archiv pozastaven, objeví se značka zaškrtnutí v jeho poli **Zastavit aktuální aktualizaci**.
- **Pokračovat v archivaci** – Obnoví zpracování vybraného archivu, který je právě pozastaven.
- **Stornovat** – Stornuje vybraný archiv. Archiv můžete stornovat, pouze pokud je jeho **Stav** nastaven na *Dokončeno*. Pokud byl archiv stornován, objeví se značka zaškrtnutí v jeho poli **Stornováno**.

## <a name="extend-your-code-to-support-custom-fields"></a>Rozšiřte svůj kód o podporu vlastních polí

Pokud tabulka `InventTrans` obsahuje jedno nebo více vlastních polí, pak možná budete muset rozšířit kód, aby je podporoval, v závislosti na tom, jak jsou pojmenována.

- Pokud vlastní pole z tabulky `InventTrans` má stejné názvy polí jako v tabulce `InventtransArchive`, znamená to, že jsou mapovány 1:1. Proto stačí vložit vlastní pole do tabulky `InventoryArchiveFields` pole skupiny `inventTrans`.
- Pokud názvy vlastních polí v tabulce `InventTrans` neodpovídají názvům polí v tabulce `InventtransArchive`, pak je třeba přidat kód k jejich mapování. Pokud máte například systémové pole s názvem `InventTrans.CreatedDateTime`, pak musíte vytvořit pole v tabulce `InventTransArchive` s jiným názvem (např. `InventtransArchive.InventTransCreatedDateTime`) a přidat rozšíření do třídy `InventTransArchiveProcessTask` a`InventTransArchiveSqlStatementHelper`, jak je znázorněno v následujícím ukázkovém kódu.

Následující ukázka kódu ukazuje příklad, jak přidat požadované rozšíření do třídy `InventTransArchiveProcessTask`.

```xpp
[ExtensionOf(classStr(InventTransArchiveProcessTask))]
Final class InventTransArchiveProcessTask_Extension
{

    protected void addInventTransFields(SysDaSelection _selectionObject)
    {
        _selectionObject.add(fieldStr(InventTrans, ModifiedBy))
            .add(fieldStr(InventTrans, CreatedBy)).add(fieldStr(InventTrans, CreatedDateTime));

        next addInventTransFields(_selectionObject);
    }


    protected void addInventTransArchiveFields(SysDaSelection _selectionObject)
    {
        _selectionObject.add(fieldStr(InventTransArchive, InventTransModifiedBy))
            .add(fieldStr(InventTransArchive, InventTransCreatedBy)).add(fieldStr(InventTransArchive, InventTransCreatedDateTime));

        next addInventTransArchiveFields(_selectionObject);
    }
}
```

Následující ukázka kódu ukazuje příklad, jak přidat požadované rozšíření do třídy `InventTransArchiveSqlStatementHelper`.

```xpp
[ExtensionOf(classStr(InventTransArchiveSqlStatementHelper))]
final class InventTransArchiveSqlStatementHelper_Extension
{
    private str     inventTransModifiedBy;  
    private str     inventTransCreatedBy;
    private str     inventTransCreatedDateTime;

    protected void initialize()
    {
        next initialize();
        inventTransModifiedBy = new SysDictField(tablenum(InventTrans), fieldNum(InventTrans, ModifiedBy)).name(DbBackend::Sql);
        inventTransCreatedDateTime = new SysDictField(tablenum(InventTrans), fieldNum(InventTrans, CreatedDateTime)).name(DbBackend::Sql);
        inventTransCreatedBy = new SysDictField(tablenum(InventTrans), fieldNum(InventTrans, CreatedBy)).name(DbBackend::Sql);
    }

    protected str buildInventTransArchiveSelectionFieldsStatement()
    {
        str     ret;

        ret = next buildInventTransArchiveSelectionFieldsStatement();
        
        if (inventTransModifiedBy)
        {
            ret += ',';
            ret += strFmt('%1',  new SysDictField(tablenum(InventTransArchive), fieldNum(InventTransArchive, InventTransModifiedBy)).name(DbBackend::Sql));
        }

        if (inventTransCreatedBy)
        {
            ret += ',';
            ret += strFmt('%1',  new SysDictField(tablenum(InventTransArchive), fieldNum(InventTransArchive, InventTransCreatedBy)).name(DbBackend::Sql));
        }

        if (inventTransCreatedDateTime)
        {
            ret += ',';
            ret += strFmt('%1',  new SysDictField(tablenum(InventTransArchive), fieldNum(InventTransArchive, InventTransCreatedDateTime)).name(DbBackend::Sql));
        }

        return ret;
    }

    protected str buildInventTransTargetFieldsStatement()
    {
        str     ret;

        ret = next buildInventTransTargetFieldsStatement();

        if (inventTransModifiedBy)
        {
            ret += ',';
            ret += strFmt('%1', inventTransModifiedBy);
        }

        if (inventTransCreatedBy)
        {
            ret += ',';
            ret += strFmt('%1', inventTransCreatedBy);
        }

        if (inventTransCreatedDateTime)
        {
            ret += ',';
            ret += strFmt('%1', inventTransCreatedDateTime);
        }

        return ret;
    }
}
```
