---
title: "Sledování provizí v pokladním místě (POS) pomocí prodejních skupin"
description: "Je běžnou praxí pro maloobchodní prodej sledovat podle zaměstnanců, kdo pracoval se zákazníkem – poskytoval pomoc, křížový prodej a zpracování transakce."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: ed4f9b3055e164600827b62d57b7a5068edb3b1a
ms.contentlocale: cs-cz
ms.lasthandoff: 01/04/2019

---

# <a name="track-commissions-in-the-point-of-sale-pos-by-using-sales-groups"></a>Sledování provizí v pokladním místě (POS) pomocí prodejních skupin

[!include [banner](includes/banner.md)]

Je běžnou praxí pro maloobchodní prodej sledovat podle zaměstnanců, kdo pracoval se zákazníkem – poskytoval pomoc, křížový prodej a zpracování transakce.

Sledování prodeje podle prodejního zástupce je měřítko prodejních schopností pracovníků, zatímco prodeje podle pokladníka znamenají měření rychlosti a účinnosti. Prodeje sledované podle obchodního zástupce se také často používají k výpočtu provize nebo jiné pobídky.

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a>Konfigurace pracovníka v POS tak, aby byl prodejním zástupcem

Když je pracovník přidán do prodejní skupiny, stane se způsobilým pro provizi a může být identifikován jako obchodní zástupce v systému. Pracovník, který není v prodejní skupině, nemá nárok na provizi a nebude uveden jako obchodní zástupce v aplikaci POS. V POS je seznam obchodních zástupců odvozen ze všech prodejních skupin, které obsahují alespoň jednoho pracovníka přiřazeného k úložišti. Seznam je uveden v POS jako kombinace ID prodejní skupiny a jména (ID: Jméno). Výchozí prodejní skupiny lze přiřadit pracovníkům na podporu scénářů, kde se prodejce rozhodne nastavit prodejního zástupce na řádcích POS automaticky. Uživatelé mohou vybrat z prodejní skupiny, jíž je pracovník členem.

## <a name="functionality-profile-settings"></a>Nastavení funkčních profilů

Existuje několik nastavení profilu funkce pro obchod, která určují tok a proces v POS zahrnující obchodní zástupce.

<table>
<thead>
<tr>
<th>Profil</th>
<th>popis</th>
</tr>
</thead>
<tbody>
<tr>
<td>Ve výchozím nastavení použít pokladníka, pokud je k dispozici</td>
<td>Pokud je tato možnost povolena, POS automaticky vyplní řádky transakcí aktuální výchozí prodejní skupinou pokladníka. Pokud pokladník nemá zadanou výchozí prodejní skupinu, hodnota nebude nastavena. Uživatel může ručně nastavit prodejní skupiny pomocí mřížky tlačítka POS.</td>
</tr>
<tr>
<td>Požadavek na výběr prodejního zástupce</td>
<td>Tato možnost má tři mezi možné hodnoty:
<ul>
<li><strong>Ne</strong> - Pokud je vybrána tato možnost, uživatel nebude vyzván k výběru skupiny daně. Hodnota může být stále nastavena pomocí výchozí prodejní skupiny pokladníka pomocí tlačítka POS mřížky.</li>
<li><strong>Začátek transakce</strong> – Pokud je tato volba vybraná a možnost <strong>Pokladník ve výchozím nastavení</strong> není povolena nebo aktuální pokladník nemá výchozí prodejní skupinu, uživatel bude vyzván k výběru prodejní skupiny na začátku každé transakce. Výběrem prodejní skupiny z tohoto příkazového řádku nastavíte všechny následné řádky vybrané prodejní skupiny jako výchozí. Uživatel může ručně nastavit prodejní skupiny pomocí mřížky tlačítka POS.</li>
<li><strong>Pro každý řádek</strong> – Pokud je tato volba vybraná a možnost <strong>Pokladník ve výchozím nastavení</strong> není povolena nebo aktuální pokladník nemá výchozí prodejní skupinu, uživatel bude vyzván k výběru prodejní skupiny po přidání jednotlivých řádků. Uživatel může ručně nastavit prodejní skupiny pomocí mřížky tlačítka POS.</li>
</ul>
</td>
</tr>
<tr>
<td>Požadovat</td>
<td>Tuto možnost lze použít, pouze pokud POS je nakonfigurován pro zadání obchodního zástupce. Pokud je povolena, uživatel bude muset před pokračováním vybrat prodejní skupinu. V opačném případě bude uživatel vyzván, ale může postup zrušit a pokračovat bez provedení výběru. Po přidání řádku může uživatel s dostatečnými oprávněními stále odebrat prodejní skupinu z řádku. V této situaci není vynucena možnost "Požadovat prodejní zástupce".</td>
</tr>
</tbody>
</table>

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a>Zobrazení informací o prodejním zástupci na obrazovce Transakce POS

Rozvržení obrazovky Transakce POS a její obsah jsou konfigurovatelné pomocí návrháře rozložení obrazovky a přiřazených rozložení obrazovky obchodům, registrům nebo pracovníkům.Pole **Prodejní zástupce** lze přidat na kartě řádky v podokně Příjem.Zobrazí se ID zadané skupiny prodeje pro každý řádek v okně transakce.

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a>Přidání operací prodejního zástupce mřížkám tlačítka operace POS

POS umožňuje uživatelům konfigurovat mříž tlačítek, které jsou součástí rozložení obrazovky poskytují přístup k operacím POS. Tlačítkům mřížky tlačítek, které se týkají obchodního zástupce, lze přiřadit následující operace POS.

| Operace                                 | popis |
|-------------------------------------------|-------------|
| Nastavit prodejního zástupce na řádku          | Tato operace POS zobrazí seznam oprávněných prodejních skupin (ID: název) pro úložiště.Výběr prodejní skupiny z tohoto seznamu nastaví hodnotu na aktuálním řádku transakce. |
| Vymazat prodejního zástupce na řádku        | Tato operace POS odstraní aktuální hodnotu prodejní skupiny z aktuálního řádku transakce. |
| Nastavení výchozího prodejního zástupce u transakce   | Tato operace POS zobrazí seznam oprávněných prodejních skupin (ID: název) pro úložiště.Výběr prodejní skupiny z tohoto seznamu nastaví výchozí hodnotu na aktuálním řádku transakce. Jakékoli existující řádky bez přiřazené prodejní skupiny řádky budou nastaveny, jakož i všechny později přidané řádky. |
| Vymazat prodejního zástupce u transakce | Tato operace POS odstraní aktuální hodnotu výchozí prodejní skupiny z aktuálního řádku transakce. To nemá vliv na žádné řádky, které již existují v transakci. |

## <a name="calculating-commissions"></a>Výpočet provizí

Provize se vypočítávají pro pracovníky v určených prodejních skupinách v době zaúčtování výkazu nebo zaúčtování prodejní objednávky.Částka provize je určena podle podílu zaměstnance na provizi, jak je definováno v prodejní skupině a nastavení výpočtu přidružené provize pro odběratele a produkty v transakci.

