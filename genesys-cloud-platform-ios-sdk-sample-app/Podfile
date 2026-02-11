platform :ios, '13.0'
use_frameworks! :linkage => :static

target 'GenesysCloudConnectDemo' do
  pod 'PureCloudPlatformClientV2', 
      :git => 'https://github.com/MyPureCloud/platform-client-sdk-ios.git',
      :tag => '186.0.0'
end

post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['CODE_SIGNING_ALLOWED'] = 'NO'
      config.build_settings['CODE_SIGNING_REQUIRED'] = 'NO'
      config.build_settings['CODE_SIGN_IDENTITY'] = ''
    end
  end
end
