---
title: přehled inkasa SEPA
description: Tento článek poskytuje informace o Jednotné oblasti pro platby v eurech (SEPA), kterou zřizuje Evropská komise.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, CustBankAccounts, CustParameters, CustTable
audience: Application User
ms.reviewer: kfend
ms.custom:
- "11144"
- intro-internal
ms.assetid: 3277c9b6-e46e-40c9-aa76-9b0449467842
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d63cac6c21ec5c5340204f409648516047bb94d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909149"
---
# <a name="sepa-direct-debit-overview"></a>přehled inkasa SEPA

[!include [banner](../includes/banner.md)]

Jednotná oblast pro platby v eurech (SEPA) je definována Evropskou komisí a určuje, že všechny elektronické platby jsou považovány za domácí bez ohledu na zemi nebo oblast, kde se osoba, podnik, nebo organizace a banka nachází. Neexistuje žádný rozdíl mezi národní a zahraniční platbou. SEPA zahrnuje 28 členských států Evropské unie (EU) plus Island, Lichtenštejnsko, Norsko, Švýcarsko, Monako a San Marino. SEPA umožňuje vytvořit jednotný trh pro platební transakce v Evropském hospodářském prostoru (EHP). Použitím SEPA se očekává snížit počet formátů plateb, se kterými banky, společnosti a jednotlivci musí pracovat.   

## <a name="what-is-the-goal-of-sepa-direct-debits"></a>Jaký je cíl přímých debetů SEPA?

Přímý debet SEPA umožňuje příjemci vybírat finanční prostředky z bankovního účtu odběratele, za předpokladu, že bylo odběratelem podepsané zmocnění uděleno příjemci. Odběratel podepisuje zmocnění autorizující příjemce vybírat platbu a vydávat bance odběratele příkaz k vyplacení shromážděných prostředků. 

Inkaso SEPA jako první vytváří platební nástroj, který lze použít pro národní a zahraniční inkaso v eurech v rámci 32 zemí/oblastí SEPA. 

K dispozici jsou dvě schémata: základní schéma inkasa SEPA a podnikatelské schéma inkasa SEPA (B2B). Oba systémy používají stejný formát souborů.

## <a name="what-is-the-core-direct-debit-scheme"></a>Co je základní schéma inkasa?
Základní schéma inkasa SEPA je základním schématem. Má následujícími atributy:
-   Převod prostředků je v eurech (i v případě, že bankovní účty mají finanční prostředky v jiných měnách).
-   Odběratel i příjemce musí mít účet u úvěrové instituce, která se nachází v oblasti SEPA.
-   Odběratel musí příjemci udělit podepsané zmocnění.
-   Platnost zmocnění končí 36 měsíců po inicializaci posledního výběru.
-   Příjemce musí uchovat pověření tak dlouho, dokud je zmocnění platné, a alespoň 14 měsíců od posledního výběru.
-   Schémata mohou být použita pro jeden (jednorázový) nebo opakující se výběr inkasa.
-   Odběratelé jsou oprávněni bez jakýchkoli dotazů obdržet refundaci až do 8 týdnů od inkasa z jejich účtu.

## <a name="what-is-the-sepa-business-to-business-b2b-direct-debit-scheme"></a>Co je podnikatelské schéma inkasa SEPA (B2B)?
Podnikatelské schéma inkasa SEPA B2B vztahuje na obchodní transakce a dále rozšiřuje základní schéma inkasa SEPA. Hlavní rozdíly:
-   Schéma inkasa SEPA B2B není povoleno, když je odběratel soukromá osoba (příjemce).
-   Zákazník nemá nárok na refundaci autorizované transakce.
-   Banky odběratele musí ověřením výběru oproti informacím zmocnění zajistit, že výběr je autorizován. Banky odběratele a odběratel se musí dohodnout na kontrole, která při každém inkasu proběhne.
-   Schéma nabízí kratší časovou ose pro prezentaci inkasa a zkracuje vratné období.

## <a name="can-i-use-the-cor1-scheme-for-direct-debit-mandates"></a>Mohu použít schéma COR1 pro zmocnění k inkasu?
Ano. Schéma COR1 můžete použít pro zmocnění k inkasu SEPA v Rakousku, Belgii, Německu, Francii, Itálii, Španělsku a Nizozemsku. Režim poskytuje kratší období před oznámením pro výběr inkasa příjemcem.

## <a name="what-are-international-bank-account-numbers-iban-and-bank-identifier-codes-bic"></a>Co je to mezinárodní číslo bankovního účtu (IBAN) a identifikační kód banky (IKB)?
Mezinárodní číslo bankovního účtu (IBAN) a identifikační kód banky (IKB) slouží pro identifikaci každého účtu v 32 zemích/oblastech SEPA. Zadejte BIC do pole Kód SWIFT a IBAN do pole IBAN. Obě pole se nachází na pevné záložce další identifikace na kartě bankovního účtu na stránce bankovních účtů. To platí pro bankovní účet příjemce i bankovní účet odběratele.

## <a name="where-do-i-enter-creditor-identifiers-direct-debit-ids"></a>Kde lze zadávat identifikátory příjemce (ID inkasa)?
V SEPA je každý příjemce identifikován jedinečným identifikátorem příjemce. Tento identifikátor umožňuje odběrateli a bance odběratele vyfiltrovat každé inkaso a poté zpracovat nebo odmítnout inkaso podle pokynů odběratele. Příjemci musí vyžádat tento identifikátor od banky. Tento identifikátor zadejte do pole ID inkasa pro bankovní účet právnické osoby.

## <a name="what-are-mandates"></a>Jaká jsou zmocnění?
Odběratel podepisuje zmocnění autorizující příjemce vybírat platbu a vydávat bance odběratele příkaz k vyplacení shromážděných prostředků. Odběratel vystaví zmocnění v tištěné podobě nebo elektronicky. Ve výchozím nastavení vyprší platnost zmocnění 36 měsíců po poslední inicializaci inkasa.

## <a name="where-do-i-specify-the-sepa-direct-debit-file-format-iso-20022"></a>Kde lze určit formát souboru s inkasem SEPA (ISO 20022)?
Formáty dat SEPA jsou založeny na normě zpráv ISO 20022. Při konfigurace způsobů platby závazků zaškrtněte políčko Obecné elektronické výkaznictví a vyberte formát platebního převodu SEPA. Tento způsob platby použijte při generování souboru plateb v deníku plateb odběratele.

## <a name="in-what-file-formats-can-i-generate-sepa-direct-debit-payment-files"></a>V jakých formátech souborů lze generovat soubory pro platbu inkasa SEPA?
Soubory elektronických plateb pro inkasa SEPA můžete generovat v těchto formátech:
-   Soubory plateb pro inkasa SEPA ve formátu PAIN.008.001.02 XML pro Belgii, Německo, Španělsko, Francii, Itálii a Nizozemsko.
-   Soubory plateb pro inkasa SEPA ve formátu PAIN.008.001.02 XM pro Rakousko a ve formátu PAIN.008.003.02 XML pro Německo.

## <a name="how-do-refunds-and-returns-work-with-sepa-direct-debits"></a>Jak fungují refundace a vrácení u inkasa SEPA?
V obou schématech inkasa SEPA mají odběratelé určitá práva na refundaci. Odběratelům je povoleno odvolat veškeré autorizované transakce v období osmi týdnů po datu splatnosti, aniž by museli uvést důvod. V případě neoprávněný transakcí je období rozšířeno na 13 měsíců od data splatnosti. Storna všech provedených plateb se provádějí ručně pomocí tlačítka Zrušit platbu na stránce Transakce odběratele.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
