# Thien2kar4.github.io
https://github.com/0562262092/Thien2kar4.github.io/new/main?readme=1
git remote add origin https://github.com/0562262092/Thien2kar4.github.io.git
git branch -M main
git push -u origin main
-- phpMyAdmin SQL Dump
-- version 5.2.1
-- https://www.phpmyadmin.net/
--
-- Máy chủ: localhost:3306
-- Thời gian đã tạo: Th6 20, 2024 lúc 10:32 AM
-- Phiên bản máy phục vụ: 10.6.17-MariaDB-cll-lve
-- Phiên bản PHP: 8.1.27

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
START TRANSACTION;
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;

--
-- Cơ sở dữ liệu: `farlmhwe_code`
--

-- --------------------------------------------------------

--
-- Cấu trúc bảng cho bảng `Banks`
--

CREATE TABLE `Banks` (
  `id` int(11) NOT NULL,
  `name` text NOT NULL,
  `chutaikhoan` text NOT NULL,
  `sotaikhoan` text NOT NULL,
  `toithieu` text NOT NULL,
  `image` text NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb3 COLLATE=utf8mb3_general_ci;

--
-- Đang đổ dữ liệu cho bảng `Banks`
--

INSERT INTO `Banks` (`id`, `name`, `chutaikhoan`, `sotaikhoan`, `toithieu`, `image`) VALUES
(8, 'TAOWEBNHANH.NET', 'TRANG TẠO SHOP TỰ ĐỘNG', '30 GIÂY CÓ TRANG WEB', '10000', 'https://taowebnhanh.net/static/media/Logovip.png'),
(9, 'KHOCODEVIP.COM', 'NƠI CUNG CẤP MÃ NGUỒN', 'UY TÍN RẺ NHẤT VIỆT NAM', '10000', 'https://i.imgur.com/yFXNTSy.jpeg'),
(10, 'DOITHE5.VN', 'HỆ THỐNG ĐỔI THẺ CÀO UY TÍN', 'CHIẾT KHẤU RẺ NHẤT ', '10000', 'https://doithe5.vn/assets/storage/images/image_VZWAM.png'),
(11, 'VPNFAST.VN', 'BÁN 4G UY TÍN', 'GIÁ RẺ NHẤT VIỆT NAM', '10000', 'https://i.imgur.com/nUKC9FX.gif');

-- --------------------------------------------------------

--
-- Cấu trúc bảng cho bảng `CpanelPackage`
--

CREATE TABLE `CpanelPackage` (
  `id` int(11) NOT NULL,
  `disk` text NOT NULL,
  `bandwidth` text NOT NULL,
  `addondomain` text NOT NULL,
  `subdomain` text NOT NULL,
  `server` text NOT NULL,
  `package` text NOT NULL,
  `price` text NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb3 COLLATE=utf8mb3_general_ci;

--
-- Đang đổ dữ liệu cho bảng `CpanelPackage`
--

INSERT INTO `CpanelPackage` (`id`, `disk`, `bandwidth`, `addondomain`, `subdomain`, `server`, `package`, `price`) VALUES
(27, '1000 MB', 'KHÔNG GIỚI HẠN', 'KHÔNG GIỚI HẠN', 'KHÔNG GIỚI HẠN', 'VN', 'VN1', '10000'),
(28, '2000 MB', 'KHÔNG GIỚI HẠN', 'KHÔNG GIỚI HẠN', 'KHÔNG GIỚI HẠN', 'VN', 'VN2', '20000');

-- --------------------------------------------------------

--
-- Cấu trúc bảng cho bảng `DataCard`
--

CREATE TABLE `DataCard` (
  `id` int(11) NOT NULL,
  `username` text NOT NULL,
  `pin` text NOT NULL,
  `serial` text NOT NULL,
  `amount` text NOT NULL,
  `type` text NOT NULL,
  `status` text NOT NULL,
  `time` text NOT NULL,
  `requestid` text NOT NULL,
  `date` text DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb3 COLLATE=utf8mb3_general_ci;

--
-- Đang đổ dữ liệu cho bảng `DataCard`
--

INSERT INTO `DataCard` (`id`, `username`, `pin`, `serial`, `amount`, `type`, `status`, `time`, `requestid`, `date`) VALUES
(13, 'taowebnhanh', '817087739484517', '10047322714624', '20000', 'VIETTEL', '2', '1718852888', '4902277681', '20/06/2024');

-- --------------------------------------------------------

--
-- Cấu trúc bảng cho bảng `Historys`
--

CREATE TABLE `Historys` (
  `id` int(11) NOT NULL,
  `username` text NOT NULL,
  `note` text NOT NULL,
  `time` text NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb3 COLLATE=utf8mb3_general_ci;

--
-- Đang đổ dữ liệu cho bảng `Historys`
--

INSERT INTO `Historys` (`id`, `username`, `note`, `time`) VALUES
(264, 'HuyMasterDesign', 'Đăng Ký Tài Khoản Thành Công', '1718453530'),
(265, 'HuyMasterDesign', 'Đăng Nhập Tài Khoản Thành Công', '1718461490'),
(266, 'HuyMasterDesign', 'Đăng Nhập Tài Khoản Thành Công', '1718474314'),
(267, 'HuyMasterDesign', 'Đăng Nhập Tài Khoản Thành Công', '1718516687'),
(268, 'taowebgame', 'Đăng Ký Tài Khoản Thành Công', '1718518119'),
(269, 'HuyMasterDesign', 'Đăng Nhập Tài Khoản Thành Công', '1718546741'),
(270, 'HuyMasterDesign', 'Thanh Toán Hosting (VN1) Thành Công, Tổng Thanh Toán: 10,000<sup>đ</sup> ', '1718549129'),
(271, 'HuyMasterDesign', 'Đăng Nhập Tài Khoản Thành Công', '1718633193'),
(272, 'HuyMasterDesign', 'Đăng Nhập Tài Khoản Thành Công', '1718633406'),
(273, '1', 'Đăng Ký Tài Khoản Thành Công', '1718681175'),
(274, 'vv', 'Đăng Ký Tài Khoản Thành Công', '1718681363'),
(275, 'HuyMasterDesign', 'Đăng Nhập Tài Khoản Thành Công', '1718791565'),
(276, 'HuyMasterDesign', 'Thanh Toán Hosting (VN1) Thành Công, Tổng Thanh Toán: 10,000<sup>đ</sup> ', '1718794936'),
(277, 'admin', 'Đăng Ký Tài Khoản Thành Công', '1718851437'),
(278, 'taowebnhanh', 'Đăng Ký Tài Khoản Thành Công', '1718852492'),
(279, 'admin', 'Đăng Nhập Tài Khoản Thành Công', '1718853103');

-- --------------------------------------------------------

--
-- Cấu trúc bảng cho bảng `Hostings`
--

CREATE TABLE `Hostings` (
  `id` int(11) NOT NULL,
  `username` text DEFAULT NULL,
  `domain` text DEFAULT NULL,
  `email` text DEFAULT NULL,
  `package` text DEFAULT NULL,
  `server` text DEFAULT NULL,
  `status` text DEFAULT NULL,
  `time` text DEFAULT NULL,
  `orvertime` text DEFAULT NULL,
  `timesuspended` text DEFAULT NULL,
  `taikhoan` text DEFAULT NULL,
  `matkhau` text DEFAULT NULL,
  `lidokhoa` text DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb3 COLLATE=utf8mb3_general_ci;

-- --------------------------------------------------------

--
-- Cấu trúc bảng cho bảng `ServerName`
--

CREATE TABLE `ServerName` (
  `id` int(11) NOT NULL,
  `name` text NOT NULL,
  `uname` text NOT NULL,
  `ssl_key` text NOT NULL,
  `backup` text NOT NULL,
  `hostname` text NOT NULL,
  `whmusername` text NOT NULL,
  `whmpassword` text NOT NULL,
  `ip` text NOT NULL,
  `nameserver1` text NOT NULL,
  `nameserver2` text NOT NULL,
  `value` text NOT NULL,
  `ghichu` text NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb3 COLLATE=utf8mb3_general_ci;

-- --------------------------------------------------------

--
-- Cấu trúc bảng cho bảng `System32`
--

CREATE TABLE `System32` (
  `id` int(11) NOT NULL,
  `date_cron` text DEFAULT NULL,
  `partner_id` text DEFAULT NULL,
  `partner_key` text DEFAULT NULL,
  `token_momo` text DEFAULT NULL,
  `modal` text DEFAULT NULL,
  `namelogo` text NOT NULL,
  `title` text DEFAULT NULL,
  `description` text DEFAULT NULL,
  `support_url` text DEFAULT NULL,
  `sitename` text DEFAULT NULL,
  `image` text DEFAULT NULL,
  `avataruser` text NOT NULL,
  `shortcut_icon` text DEFAULT NULL,
  `script` text DEFAULT NULL,
  `value_hosting` text DEFAULT NULL,
  `value_domain` text DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb3 COLLATE=utf8mb3_general_ci;

--
-- Đang đổ dữ liệu cho bảng `System32`
--

INSERT INTO `System32` (`id`, `date_cron`, `partner_id`, `partner_key`, `token_momo`, `modal`, `namelogo`, `title`, `description`, `support_url`, `sitename`, `image`, `avataruser`, `shortcut_icon`, `script`, `value_hosting`, `value_domain`) VALUES
(1, '1718854189', 'NULL', 'NULL', 'NULL', '', 'KHOCODEVIP', 'Hệ Thống Bán Hosting Giá Rẻ Cấu Hình Siêu Khỏe', 'Hệ Thống Bán Hosting Giá Rẻ Cấu Hình Siêu Khỏe', 'https://portal.vpnfast.vn/reseller', 'https://khocodevip.com', 'https://i.imgur.com/guSdNlL.jpg', 'https://sunihost.com/assets/images/avt.png', '/assets/images/favicon-32x32.png', '', 'on', 'on');

-- --------------------------------------------------------

--
-- Cấu trúc bảng cho bảng `TranIDMomo`
--

CREATE TABLE `TranIDMomo` (
  `id` int(11) NOT NULL,
  `requestid` text NOT NULL,
  `amount` text NOT NULL,
  `comment` text NOT NULL,
  `time` text NOT NULL,
  `nameBank` text NOT NULL,
  `status` text NOT NULL,
  `date` text DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb3 COLLATE=utf8mb3_general_ci;

-- --------------------------------------------------------

--
-- Cấu trúc bảng cho bảng `Users`
--

CREATE TABLE `Users` (
  `id` int(11) NOT NULL,
  `name` text NOT NULL,
  `username` text NOT NULL,
  `password` text NOT NULL,
  `email` text NOT NULL,
  `monney` text NOT NULL,
  `monneydatieu` text NOT NULL,
  `monneydanap` text NOT NULL,
  `time` text NOT NULL,
  `level` text DEFAULT NULL,
  `date_online` text DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb3 COLLATE=utf8mb3_general_ci;

--
-- Đang đổ dữ liệu cho bảng `Users`
--

INSERT INTO `Users` (`id`, `name`, `username`, `password`, `email`, `monney`, `monneydatieu`, `monneydanap`, `time`, `level`, `date_online`) VALUES
(61, 'LE VAN KHANH', 'admin', '21232f297a57a5a743894a0e4a801fc3', 'hotro.autosubre@gmail.com', '0', '0', '0', '1718851437', 'admin', '1718853216'),
(62, 'TAOWEBNHANH.NET', 'taowebnhanh', 'b56ae2a46822bddd838c2b0354a43d02', 'taowebnhanh@gmail.com', '0', '0', '0', '1718852492', 'admin', '1718854312');

--
-- Chỉ mục cho các bảng đã đổ
--

--
-- Chỉ mục cho bảng `Banks`
--
ALTER TABLE `Banks`
  ADD PRIMARY KEY (`id`);

--
-- Chỉ mục cho bảng `CpanelPackage`
--
ALTER TABLE `CpanelPackage`
  ADD PRIMARY KEY (`id`);

--
-- Chỉ mục cho bảng `DataCard`
--
ALTER TABLE `DataCard`
  ADD PRIMARY KEY (`id`);

--
-- Chỉ mục cho bảng `Historys`
--
ALTER TABLE `Historys`
  ADD PRIMARY KEY (`id`);

--
-- Chỉ mục cho bảng `Hostings`
--
ALTER TABLE `Hostings`
  ADD PRIMARY KEY (`id`);

--
-- Chỉ mục cho bảng `ServerName`
--
ALTER TABLE `ServerName`
  ADD PRIMARY KEY (`id`);

--
-- Chỉ mục cho bảng `System32`
--
ALTER TABLE `System32`
  ADD PRIMARY KEY (`id`);

--
-- Chỉ mục cho bảng `TranIDMomo`
--
ALTER TABLE `TranIDMomo`
  ADD PRIMARY KEY (`id`);

--
-- Chỉ mục cho bảng `Users`
--
ALTER TABLE `Users`
  ADD PRIMARY KEY (`id`);

--
-- AUTO_INCREMENT cho các bảng đã đổ
--

--
-- AUTO_INCREMENT cho bảng `Banks`
--
ALTER TABLE `Banks`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=12;

--
-- AUTO_INCREMENT cho bảng `CpanelPackage`
--
ALTER TABLE `CpanelPackage`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=30;

--
-- AUTO_INCREMENT cho bảng `DataCard`
--
ALTER TABLE `DataCard`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=14;

--
-- AUTO_INCREMENT cho bảng `Historys`
--
ALTER TABLE `Historys`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=280;

--
-- AUTO_INCREMENT cho bảng `Hostings`
--
ALTER TABLE `Hostings`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=15;

--
-- AUTO_INCREMENT cho bảng `ServerName`
--
ALTER TABLE `ServerName`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=8;

--
-- AUTO_INCREMENT cho bảng `System32`
--
ALTER TABLE `System32`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=2;

--
-- AUTO_INCREMENT cho bảng `TranIDMomo`
--
ALTER TABLE `TranIDMomo`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT cho bảng `Users`
--
ALTER TABLE `Users`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=63;
COMMIT;

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;

