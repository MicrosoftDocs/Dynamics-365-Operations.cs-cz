---
title: Vylepšení v řízení hotovosti
description: Toto téma popisuje vylepšení řízení hotovosti v POS pro Dynamics 365 Commerce.
author: anpurush
ms.date: 05/21/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: f878f39e8e9913edbe1da192e199090139a88adb6b7ed9a1e9b779c5748171b5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735647"
---
# <a name="cash-management-improvements"></a>Vylepšení v řízení hotovosti

[!include [banner](includes/banner.md)]


Řízení hotovosti je klíčovou funkcí pro maloobchodní prodejce ve fyzických prodejnách. Maloobchodní prodejci chtějí, aby jejich obchody měly systémy, které jim mohou poskytnout úplnou sledovatelnost a zodpovědnost za hotovost a její pohyb mezi různými registračními pokladnami a pokladníky v obchodě. Musí být schopni odsouhlasit všechny rozdíly a určit zodpovědnosti.


Microsoft Dynamics 365 Commerce má schopnosti řízení hotovosti ve své aplikaci POS. Avšak ve verzích aplikace Retail starších než 10.0.3 funkce řízení hotovosti není dostatečně robustní, aby poskytovala úplnou sledovatelnost pohybů hotovosti v obchodech. Ačkoliv maloobchodní prodejci mohou odsouhlasit hotovost obchodu, nemohou v případě nesrovnalostí v hotovosti přesně stanovit zodpovědnost.


V aplikaci Retail verze 10.0.3 a novějších získají maloobchodní prodejci sledovatelnost pro zpracování hotovosti. Jako součást této sledovatelnosti mohou maloobchodní prodejci definovat trezory, vytvářet dvoustranné hotovostní transakce a odsouhlasit transakce řízení hotovosti.

## <a name="set-up-traceability-and-define-safes"></a>Nastavení sledovatelnosti a definování trezorů

Chcete-li nastavit novou funkci řízení hotovosti, nakonfigurujte funkční profil pro obchody pomocí následujících kroků.

1. Přejděte na **Retail and Commerce \> Nastavení kanálu \> Nastavení POS \> Profily POS \> Funkční profily** a zvolte funkční profil, který je navázaný na obchody, u kterých chcete provést dostupná vylepšení pro řízení hotovosti.
2. Na záložce s náhledem **Funkce** funkčního profilu v nabídce **Rozšířené řízení hotovosti** nastavte možnost **Povolit sledovatelnost hotovosti** na **Ano.**
3. Chcete-li nastavit trezory, přejděte **Retail and Commerce \> Kanály \> Obchody \> Všechny maloobchody** a vyberte obchod.
4. Na stránce **Obchody** v podokně akcí na kartě **Nastavení** ve skupině **Nastavení** vyberte **Trezory**. Pomocí této možnosti lze definovat a udržovat více trezorů pro obchod.
4. Před použitím funkce je nutné spustit úlohu plánu distribuce **1070 - konfigurace kanálu** a synchronizovat tyto konfigurace do databáze kanálů.

## <a name="additional-cash-management-changes"></a>Další změny řízení hotovosti

Ve verzi 10.0.3 aplikace Retail a novějších jsou rovněž poskytnuty následující možnosti související s hotovostními transakcemi:

- Uživatel, který je vyzván k deklaraci počáteční částky, musí zadat zdroj hotovosti. Uživatel může vyhledat dostupné trezory, které jsou definovány v obchodě, a vybrat trezor, ze kterého se hotovost vyzvedává, aby mohla být vložena do registrační pokladny.
- Uživatel, který provádí operaci odebrání úhrady, je vyzván, aby vybral ze seznamu otevřených transakcí plovoucího zůstatku tu transakci, proti které se provádí operace. Pokud v systému neexistuje odpovídající plovoucí zůstatek, uživatel může vytvořit nepropojenou transakci odebrání úhrady.
- Operace plovoucího zůstatku vyzve uživatele, aby vybral ze seznamu otevřených transakcí odebrání úhrady tu transakci, proti které se provádí operace plovoucího zůstatku. Pokud v systému neexistuje odpovídající odebrání úhrady, uživatel může vytvořit nepropojenou transakci plovoucího zůstatku.
- Uživatel, který provádí odvod do trezoru, je vyzván k výběru trezoru, do kterého se odvádí hotovost.
- U trezorů, které jsou definovány v obchodě, mohou uživatelé spravovat operace, jako je například deklarování počáteční částky, provedení plovoucího zůstatku, provedení odebrání úhrady a odvod do banky.
- Pro uživatele, kteří mají příslušná oprávnění, zobrazují operace správy směn zůstatky hotovosti aktivních směn, pozastavených směn a směn uzavřených bez zadání částky.
- Chcete-li odsouhlasit hotovostní transakce v rámci směny nebo napříč směnami, vyberte směnu k odsouhlasní a pak zvolte **Odsouhlasit**. Otevřené zobrazení ukazuje seznam odsouhlasených a neodsouhlasených transakcí na samostatných kartách. Z tohoto zobrazení mohou uživatelé buď vybrat neodsouhlasené transakce a odsouhlasit je, nebo vybrat dříve odsouhlasené transakce a zrušit jejich odsouhlasení.
- Pokud se při odsouhlasení nevyrovnává vybraná transakce, uživatel musí zadat popis důvodu nevyrovnaného odsouhlasení. Uživatelé mohou vybrat jednu transakci a odsouhlasit ji s odpovídajícím popisem důvodu podle potřeby.
- Uživatelé mohou pokračovat v odsouhlasení a zrušení odsouhlasení transakcí, dokud není směna uzavřena. Po uzavření směny nelze zrušit odsouhlasení transakcí.
- Když se uživatel rozhodne uzavřít směnu, aplikace Commerce ověří, zda ve směně neexistují žádné neodsouhlasené transakce řízení hotovosti. Uživatelé nemohou uzavřít směnu, pokud existují transakce, u nichž bylo zrušeno odsouhlasení.


[!INCLUDE[footer-include](../includes/footer-banner.md)]