---
title: Odložené zpracování ručního pohybu zásob
description: Toto téma popisuje, jak použít odložené zpracování ručního pohybu zásob v Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
ms.date: 04/27/2021
ms.topic: article
ms.search.form: WHSWorkProcessingPolicy, WHSWorkDeferredPutProcessingTask
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: Mirzaab
ms.search.validFrom: 2021-04-27
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f5c9ba7079895feeb0c171f2021479587aa13cc9
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/09/2021
ms.locfileid: "7777659"
---
# <a name="deferred-processing-of-manual-inventory-movement"></a>Odložené zpracování ručního pohybu zásob

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak použít odložené zpracování ručního pohybu zásob v Microsoft Dynamics 365 Supply Chain Management.

Odložené zpracování umožňuje pracovníkům skladu pokračovat v práci i v době, kdy na pozadí běží operace vložení. Odložené zpracování je užitečné v případě, kdy server může mít v době zpracování občasný nebo neplánovaný nárůst doby zpracování a ta může ovlivnit produktivitu pracovníka. Typ práce *Pohyb zásob* byl nyní přidán do sady pracovních typů, které tato funkce podporuje.

Zpracování na pozadí je dosaženo použitím [Funkce zpracování událostí aplikace ve skladu](warehouse-app-events.md).

## <a name="turn-on-this-feature-for-your-system"></a>Zapnutí této funkce ve vašem systému

Chcete-li tuto funkci zpřístupnit, zapněte následující funkce ve [správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md): Musíte je zapnout v tomto pořadí:

1. Blokování práce pro celou organizaci (od Supply Chain Management verze 10.0.21 je tato funkce povinná, takže je ve výchozím nastavení zapnutá a nelze ji znovu vypnout).
1. Zpracovat události aplikace skladu
1. Odložené operace Put
1. Odložené zpracování ruční operace přesunu zásob

## <a name="configure-the-work-processing-policies"></a>Konfigurace zásad zpracování pracovních postupů

Chcete-li použít odložené zpracování, je nutné nastavit a použít zásady zpracování pracovních postupů. U odloženého zpracování [Odložené zpracování funkce skladové práce](deferred-put.md) podporuje následující typy práce: *Prodejní objednávka*, *Problém s převodem objednávky* a *Doplňování*. Funkce *Odložené zpracování operace ručního pohybu zásob* přidává nový typ práce: *Pohyb zásob*.

Pokud chcete nastavit zásady zpracování práce, postupujte následovně.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Práce \> Pracovní zásady zpracování**.
1. Vyberte existující zásady v seznamu nebo vytvořte novou zásadu výběrem **Nový** v podokně akcí. Záhlaví každé zásady má následující pole:

    - **Název pracovní zásady zpracování** – Název pracovní zásady zpracování.
    - **Popis** – Popis pracovní zásady zpracování.

1. Na rychlé kartě **Pravidla zpracování** nastavte kolekci pravidel, na která budou zásady platit. Pomocí následujících tlačítek na panelu nástrojů můžete podle potřeby přidávat a odebírat pravidla. U každého pravidla je třeba nastavit tato pole:

    - **Typ pracovního příkazu** – Vyberte typ práce, pro který zásada platí.
    - **Úkon** – Vyberte operaci, kterou zásada používá ke zpracování. Pokud jste vybrali *Pohyb zásob* v poli **Typ pracovního příkazu**, nemusíte toto pole nastavovat, protože operace vyzvednutí i vložení jsou zpracovány jako jedna událost.
    - **Metoda zpracování práce** – Vyberte metodu, která se používá ke zpracování pracovní linky. Pokud vyberete *Okamžitě*, chování se podobá chování, když pro zpracování řádku nejsou použity žádné zásady zpracování práce. Pokud vyberete *Odložený*, systém použije odložené zpracování, které používá dávkový rámec.
    - **Prahová hodnota odloženého zpracování** – Pokud nastavíte toto pole na *0* (nula), neexistuje žádná prahová hodnota. V tomto případě se použije *odložené* zpracování, pokud je to možné. Pokud je výpočet specifické prahové hodnoty nižší než práh, použije se metoda *Okamžitě*. V opačném případě se použije metoda *Odloženo*, pokud je to možné. V případě práce související s prodejem a převodem je prahová hodnota vypočtena jako počet přidružených řádků zatížení zdroje, které jsou pro práci zpracovávány. Pro práci doplnění se práh vypočítá jako počet řádků práce, které jsou doplněny prací. Nastavením prahové hodnoty, například *5* pro prodej, zajistíte, že nebudou menší práce, které mají méně než pět počátečních zdrojových řádků vytížení, používat odložené zpracování, ale větší práce jej budou používat. Prahová hodnota se uplatní pouze v případě, že je pole **Metoda zpracování práce** nastavena na hodnotu *Odloženo*.
    - **Skupina dávek odloženého zpracování** – Určete skupinu dávek, která se používá ke zpracování. Pokud jste vybrali *Pohyb zásob* v poli **Typ pracovního příkazu**, toto pole nemusíte nastavovat, protože skupina dávek je vybrána v dialogovém okně **Zpracovat události aplikace skladu**.

## <a name="assign-the-work-creation-policy"></a>Přiřazení zásad vytváření pracovních míst

Podrobnosti o tom, jak přiřadit zásadu vytváření práce, najdete v části [Odložené zpracování skladových prací](deferred-put.md).

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Nastavit dávkovou úlohu pro zpracování událostí aplikace skladu

Chcete-li použít proces *Odložené zpracování operace ručního pohybu zásob*, nastavte naplánovanou dávkovou úlohu.

1. Přejděte na **Správa skladu \> Periodické úkoly \> Zpracovat události aplikace skladu**.
1. V dialogovém okně **Zpracovat události aplikace skladu** na pevné záložce **Spustit na pozadí** nastavte u možnosti **Dávkové zpracování** hodnotu *Ano*.
1. Vyberte **Opakování** a nastavte plán běhu, který splňuje požadavky vašeho podnikání.
1. V každém dialogovém okně vyberte **OK**.

## <a name="inquire-about-the-warehouse-app-events"></a>Prošetřování událostí aplikace skladu

Frontu událostí a zprávy o událostech generované aplikací skladu si můžete zobrazit přechodem na **Řízení skladu \> Dotazy a zprávy \> Protokoly mobilních zařízení \> Události aplikace skladu**.

Zprávy události *Pohyb zásob* budou mít stav *Ve frontě*, když jsou poprvé vytvořeny. Tento sta znamená, že dávková úloha **Zpracovat události aplikace skladu** vyzvedne zprávy události a zpracuje je. Když je stav události aktualizován na *Dokončeno*, všechny související události jsou odstraněny z fronty.

Všechny události *Pohyb zásob* se shromažďují v rámci jedné kolekce pro každý typ události a sklad.

Dávková úloha zpracuje události aplikace skladu podle opakování, které je nastaveno v dialogovém okně **Zpracovat události aplikace skladu**. Dokud tedy nebude zpracována zpráva, můžete ID skladu vyhledat hledáním v poli **Identifikátor**.

Podrobnosti zprávy obsahují podrobnosti o pohybu (například umístění „z“ a „do“).

Další informace viz [Zpracování událostí aplikace skladu](warehouse-app-events.md).

## <a name="configure-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a>Konfigurace nabídky mobilního zařízení pro přeskočení zásady odloženého zpracování

Podrobnosti o tom, jak nakonfigurovat nabídku mobilního zařízení tak, aby se přeskočily zásady odloženého zpracování, najdete v části [Odložené zpracování skladových prací](deferred-put.md).

## <a name="impact-on-closed-work-dates"></a>Dopad na data uzavřené práce

Podrobnosti o dopadu na data uzavřených prací viz [Odložené zpracování skladových prací](deferred-put.md).

## <a name="additional-resources"></a>Další prostředky

- [Odložené zpracování práce skladu](deferred-put.md)
- [Zpracování události aplikace skladu](warehouse-app-events.md)
- [Nastavení mobilních zařízení pro práci ve skladu](configure-mobile-devices-warehouse.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
