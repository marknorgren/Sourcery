# Uncomment this line to define a global platform for your project
platform :osx, '10.11'

workspace 'Sourcery.xcworkspace'
use_frameworks!
inhibit_all_warnings!

def meta
  pod 'SwiftLint'
end

def test_pods
  pod 'Quick'
  pod 'Nimble'
end

def pathkit
  pod 'PathKit', '1.0.0'
end

target 'TemplatesTests' do
  project 'Templates/Templates.xcodeproj'
  meta
  test_pods
end
target 'CodableContextTests' do
  project 'Templates/Templates.xcodeproj'
  meta
  test_pods
end

target 'Sourcery' do
  pod 'Stencil', '0.14.0'
  pod 'StencilSwiftKit', :git =>'git@github.com:SwiftGen/StencilSwiftKit.git', :branch => 'stable'
  pod 'Commander', '0.7.0'
  pathkit
  pod "xcodeproj", :git =>'git@github.com:tuist/XcodeProj.git', :tag => '7.0.0'
  pod 'SourceKittenFramework', '0.23.1'
  pod 'Yams', '2.0.0'

  target 'SourceryTests' do
    inherit! :search_paths
    test_pods
  end
end

target 'SourceryJS' do
  pathkit
end

target 'SourcerySwift' do
  pathkit
end

target 'SourceryUtils' do
  pathkit
end

target 'SourceryFramework' do
  pathkit
  pod 'SourceKittenFramework', '0.23.1'
end
