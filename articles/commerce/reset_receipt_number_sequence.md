---
title: Resetování čísel příjemek
description: V tomto tématu je popsán postup při obnovení čísel účtenek, která se používají pro různé akce k požadovanému datu (například fiskální rok nebo kalendářní rok).
author: ShalabhjainMSFT
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Commerce
ms.author: asharchw
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Application update 10.0.9
ms.openlocfilehash: 855c39f15db6de8fac1f0cd4667eec485c70542b9aebde0d7085e2703f4609bb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733862"
---
# <a name="reset-receipt-numbers"></a>Resetování čísel příjemek 

[!include [banner](includes/banner.md)]

> [!NOTE]
> Požaduje se, abyste vybrali vlastnost **Nezávislé pořadí** pro všechny typy příjmu v profilu funkce před použitím této funkce. Časové pásmo systému zařízení, ve kterém se používá POS, by se také mělo shodovat s odpovídajícím časovým pásmem úložiště. Z důvodu těchto omezení doporučujeme, abyste tuto funkci nepoužívali v produkčním prostředí – pracujeme na vyřešení těchto problémů v budoucím vydání. 

Maloobchodní prodejci generují čísla účtenek pro různé akce v obchodě, jako jsou například hotovostní transakce a realizované transakce, transakce vratek, objednávky zákazníků, nabídky a platby. Ačkoliv maloobchodní prodejci definují vlastní formáty účtenek, některé země nebo regiony mají právní předpisy, které omezují tyto formáty účtenek. Tato pravidla mohou například omezit počet znaků na příjemce, požadovat po sobě jdoucí čísla příjmu, omezit některé speciální znaky nebo požadovat obnovení čísel účtenek na začátku roku. Aplikace Microsoft Dynamics 365 Commerce usnadňuje správu čísel příjemek, aby maloobchodní prodejci plnili zákonné požadavky. Toto téma vysvětluje, jak používat funkci pro obnovení čísel účtenek.

V aplikaci Commerce mohou být formáty účtenek alfanumerické. Do nich můžete vložit statický i dynamický obsah. Statický obsah zahrnuje abecední znaky, čísla a speciální znaky. Dynamický obsah obsahuje jeden nebo více znaků reprezentujících informace, jako je číslo obchodu, číslo terminálu, datum, měsíc, rok a číselné řady, které se automaticky zvyšují. Formáty jsou definovány v části **číslování účtenek** funkčního profilu. V následující tabulce jsou popsány znaky představující dynamický obsah.

| Znaky | Popis |
|------------|-------------|
| S          | Znak **S** se používá pro číslo obchodu. Je-li například obchod HOUSTON1 číslovaný, bude se u účtenky **v** poli Formát služby zabezpečené úložištěm zobrazovat hodnota ON1. Ve formátu **SSSSS** je pro příjemku uvedeno "STON1". |
| T          | Znak **T** se používá pro číslo terminálu. Pokud je například terminál číslovaný 0001, formát **TTTT** ukazuje na příjemce 0001. |
| K          | Znak **C** se používá pro číslo ID zaměstnance. Má-li například zaměstnanec ID 000160, zobrazí se na příjemce ve formátu **CCCC** "0160". |
| ddd        | Znaky **ddd** odpovídají dni v roce od 1 do 366. Například pro 15. ledna zobrazuje formát **ddd** na příjemce "015". |
| MM         | Znaky **MM** se používají pro měsíc vyjádřený dvěma číslicemi. Například pro leden zobrazuje formát **MM** na příjemce "01". |
| DD         | Znaky **DD** se používají pro den v měsíci vyjádřený dvěma číslicemi. Například pro 15. ledna zobrazuje formát **DD** na příjemce "15". |
| RR         | Znaky **RR** se používají pro rok vyjádřený dvěma číslicemi. Například v kterémkoli měsíci v roce 2020 je formát **RR** pro účtenku označen znakem "20". |
| \#         | Pro sekvenční číslování se používá číselný znak (**\#**). Například formát **####** ukazuje na příjmu hodnoty "0001," "0002," "0003," atd. |

Postupné číslování příjemky lze resetovat k určitému datu. Pro první transakci, která se objeví po 12:00 dopoledne k vybranému datu resetování, pak systém znovu nastaví číselnou řadu příjemky na 1. Můžete také určit, zda má být vynulován pouze jeden čas, nebo zda se bude opakovat každý rok. Je-li zadáno roční opakování, dojde k automatickému obnovení každého roku, dokud se jej maloobchodní prodejce nerozhodne zastavit. 

Chcete-li zapnout resetování, postupujte následujícím způsobem.

1. Přejděte na **Maloobchodní a velkoobchodní prodej \> Instalace kanálu \> Nastavení POS \> Profily POS \> Funkční profily**.
1. Na pevné záložce **Číslování příjemky** vyberte **Obnovit datum resetování čísel**.
1. V rozevíracím dialogovém okně v poli **Resetovat datum** vyberte budoucí datum, kdy má dojít k vymazání.
1. V poli **Resetovat typ příjemky** vyberte **pouze jednorázově** nebo **Ročně**.
1. Vyberte **OK**.

![Výběr data obnovení účtenky.](media/Enable_receipt_reset.png "Výběr data obnovení účtenky")

Poté, co vyberete datum, bude zobrazeno ve sloupci **další datum resetování čísla příjemky**. Datum resetování lze použít pro všechny typy transakcí příjemky. Proto bude číselná řada příjmu vynulována pro všechny typy příjemek.

Po obdržení nového data je vynulováno číslo příjemky pro první transakci každého typu. Kromě toho ve funkčním profilu je datum přesunuto ze sloupce **Datum resetování čísla příjemky** do sloupce **Datum resetování aktuálního čísla příjemky**. Tato změna znamená, že pokud není registrační pokladna pro datum resetování použita, bude číslo účtenky vynulováno při příštím použití *registru*. Například 3. prosince 2019, vyberte jako datum resetování **1. ledna 2020**. 1. ledna, když registr provede první transakci, bude číslo příjemky vynulováno. Jeden registr se však během prosince a ledna vůbec nepoužívá, ale začne se používat v únoru. V tomto případě, protože byla definována akce resetování, bude číslo příjmu pro tento registr vynulováno, jakmile registr provede první transakci v únoru.

Chcete-li vymazat budoucí data resetování, můžete použít funkci **Vymazat datum resetování** k vymazání budoucích dat resetování. Pokud však k datu resetování došlo v minulosti, nelze je vrátit zpět. V důsledku toho bude obnovení přesto probíhat u všech registrů, u nichž dosud nedošlo k resetování.

> [!NOTE]
> V závislosti na zvoleném datu resetování a na formátu účtenky mohou být k dispozici duplicitní čísla příjmu. Ačkoli systém Retail POS může tyto situace zpracovat, zvyšují dobu potřebnou ke zpracování vratek, protože prodejci musí vybírat mezi duplicitními příjmy. Další komplikace související s čištěním dat mohou nastat v případě, že duplicitní příjemky nebyly naplánovány. Proto doporučujeme, abyste používali dynamické datové znaky (například **DDD**, **mm**, **DD** a **RR**), aby se zabránilo výskytu duplicitních čísel příjmu po resetování.


[!INCLUDE[footer-include](../includes/footer-banner.md)]