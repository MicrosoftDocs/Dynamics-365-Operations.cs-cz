---
title: Dokončení, publikování a nasazení funkce globalizace
description: Toto téma obsahuje informace o funkci životním cyklu funkcí globalizace.
author: dkalyuzh
ms.date: 12/15/2021
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
ms.openlocfilehash: 21e03660387c7e715bc0f4cb1dbcd3ec9ec6cee2
ms.sourcegitcommit: 1843235766b6f8cf950a13a310e9f4f2f53c59a4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/07/2022
ms.locfileid: "8554554"
---
# <a name="complete-publish-and-deploy-a-globalization-feature"></a>Dokončení, publikování a nasazení funkce globalizace

[!include [banner](../includes/banner.md)]

## <a name="electronic-invoicing-feature-versions"></a>Verze funkce elektronické fakturace

Funkce elektronické fakturace mají verze. Když je vytvořena nová verze, číslo verze se automaticky zvýší.

Verze funkcí elektronické fakturace dodržují životní cyklus, který má až tři stavy:

- **Návrh** – Když má verze funkce tento stav, můžete upravit její konfigurační atributy a její artefakty (například konfigurace formátu souboru).
- **Dokončeno** – Tento stav znamená, že jste dokončili úpravy verze funkce a nehodláte v ní provádět žádné další aktualizace. Když má verze funkce tento stav, nemůžete už upravovat funkci ani žádnou z jejích komponent.
- **Publikováno** – Tento stav znamená, že verze funkce byla publikována do globálního úložiště, které je přidruženo k vaší organizaci. Když má verze funkce tento stav, nemůžete už upravovat funkci ani žádnou z jejích komponent.

Pro novou verzi funkce elektronické fakturace můžete zadat datum **Účinné od**. Tímto způsobem můžete definovat výchozí verzi, kterou lze použít nebo kterou lze přepsat, když je funkce nasazena do prostředí služby.

Chcete-li změnit stav verze funkce elektronické fakturace, postupujte takto.

1. Přihlaste se ke svému účtu Regulatory Configuration Service (RCS).
2. V pracovním prostoru **Funkce globalizace** v části **Funkce** vyberte dlaždici **Elektronická fakturace**.
3. Na levé straně stránky **Funkce elektronické fakturace** vyberte funkci elektronické fakturace.
4. Na kartě **Verze** v pravé části stránky vyberte verzi.
5. Vyberte příkaz **Změnit stav** a poté vyberte **Dokončeno** (pokud je aktuální stav **Návrh**) nebo **Publikováno** (pokud je aktuální stav **Dokončeno**).
6. V dialogovém okně vyberte **Ano** a potvrďte tak požadavek.

Ruční změna ze stavu **Dokončeno** na stav **Publikováno** je volitelná. Verze funkcí elektronické fakturace se automaticky aktualizují na stav **Publikováno**, když jsou nasazeny do prostředí služby.

Stav můžete sledovat ve sloupci **Stav verze funkce** na kartě **Verze**.

## <a name="deploy-feature-versions"></a>Nasazení verzí funkcí

V RCS použijte příkaz **Nasadit** k publikování verze funkce elektronické fakturace do cílového servisního prostředí nebo připojené aplikace.

1. Na levé straně stránky **Funkce elektronické fakturace** vyberte funkci elektronické fakturace.
2. Na kartě **Verze** na pravé straně stránky vyberte verzi funkce elektronické fakturace, kterou chcete nasadit do prostředí služby nebo připojené aplikace. Vybraná verze musí mít stav **Dokončeno** nebo **Publikováno**.
3. Vyberte **Nasadit** a poté vyberte jednu nebo obě následující možnosti k definování cíle nasazení:

    - **Připojená aplikace** – Konfigurace poskytovaná nastavením aplikace je napsána v instanci Microsoft Dynamics 365 Finance nebo Dynamics 365 Supply Chain Management, která s ní byla dříve spojena.
    - **Prostředí služby** – Verze funkce elektronické fakturace je nasazena do prostředí služby. Elektronická fakturace je poté připravena přijímat a zpracovávat elektronické dokumenty, které odesílají aplikace Finance nebo Supply Chain Management.

> [!NOTE]
> Obvykle změníte parametry funkce Elektronické výkaznictví (ER), která musí být nasazena do prostředí služby. Změny v připojené aplikaci budou vzácné. Nové verze byste měli nasadit do připojené aplikace pouze tehdy, když změníte odpovídající parametry vaší aplikace.

Chcete-li zjistit, zda je určitá verze funkce elektronické fakturace nasazena do konkrétního prostředí, přečtěte si informace na kartě **Prostředí**.

## <a name="remove-feature-versions"></a>Odstranění verzí funkce

V RCS můžete příkazem **Zrušit** odebrat konkrétní verzi funkce elektronické fakturace z prostředí služby, pokud tam byla nasazena.

> [!IMPORTANT]
> Tlačítko **Zrušit** funguje pouze pro servisní prostředí. Z připojené aplikace neodstraní nic, co se týká funkce elektronické fakturace.

## <a name="rebase-electronic-invoicing-features"></a>Přeskládání funkcí elektronické faktury

Když je jedna funkce elektronické fakturace odvozena od jiné, můžete příkazem **Přeskládání** aktualizovat odvozený prvek změnami, které byly provedeny v původní (nadřazené) funkci.

Chcete-li přeskládat odvozenou verzi funkce, kterou jste vytvořili, postupujte takto.

1. Získejte nejnovější verzi funkce importem z globálního úložiště. Další informace najdete v tématu [Import funkce z globálního úložiště](e-invoicing-import-feature-global-repository.md).
2. V seznamu funkcí vyberte funkci, kterou chcete obnovit.
3. Na kartě **Verze** vyberte **Nová** a vytvořte tak nový koncept.
4. Vyberte **Přeskládat**.
5. V dialogovém okně **Přeskládat** vyberte verzi funkce, která je základem.
6. Vyberte **OK**.
7. Zkontrolujte součásti funkce a proveďte požadované změny.
8. Vyberte **Změnit stav** k dokončení funkce přeskládání. Po dokončení přeskládání můžete provádět další akce.

## <a name="get-a-specific-version-of-electronic-invoicing-features"></a>Získání konkrétní verze funkce elektronické fakturace

Když vytvoříte novou verzi funkce elektronické fakturace, systém vytvoří kopii nejnovější verze funkce. Chcete-li použít dřívější verzi funkce jako základ pro novou verzi, vyberte verzi a poté vyberte příkaz **Získat tuto verzi**. Vytvoří se nový koncept funkce, který je kopií vybrané verze.
